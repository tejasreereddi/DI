# DI
This is Teja Sree Reddy working   
In Dynamic Informatics.in 
AS a techno-functional COnsultant 
table 50100 custcategory

{
    // DrillDownPageId = 
    //LookupPageId=
    Caption = 'Customer Category';


    DataClassification = ToBeClassified;

    fields
    {
        field(1; No; Code[20])
        {
            DataClassification = CustomerContent;
            Caption = 'NO';
            trigger OnValidate();
            begin

            end;


        }
        field(2; Description; Text[50])
        {
            DataClassification = CustomerContent;
            Caption = 'Description';
        }
        field(3; Default; Boolean)
        {
            DataClassification = CustomerContent;
            Caption = 'default';
            // CaptionML='default';

        }
        field(4; TotalCustomersForCategory; Integer)
        {
            FieldClass = FlowField;
            //CalcFormula=count(Customer where(CustCategory=field(No)));

        }
        field(5; EnableNewsletter; Option)
        {
            OptionMembers = " ","Full",":Limited";
            OptionCaption = ',Full,Limited';
            Caption = 'Enable Newsletter';
            DataClassification = CustomerContent;

        }
        field(6; FreeGiftsAvailable; Boolean)
        {
            DataClassification = CustomerContent;
            Caption = 'Free Gifts Available';


        }


    }



    keys
    {
        key(PK; No)
        {
            Clustered = true;
        }
    }

    var
        myInt: Integer;

    trigger OnInsert()
    begin

    end;

    trigger OnModify()
    begin

    end;

    trigger OnDelete()
    begin

    end;

    trigger OnRename()
    begin

    end;

}