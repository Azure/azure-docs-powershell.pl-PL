---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 59CDE74B-EFB3-4904-A482-466B0EA17F4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a787193669cab32a43b7c9b9eb2010a6e545539b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055190"
---
# <span data-ttu-id="22db7-101">New-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="22db7-101">New-AzureAutomationAccount</span></span>

## <span data-ttu-id="22db7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="22db7-102">SYNOPSIS</span></span>

<span data-ttu-id="22db7-103">Tworzy konto usługi Automation.</span><span class="sxs-lookup"><span data-stu-id="22db7-103">Creates an Automation account.</span></span>

## <span data-ttu-id="22db7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="22db7-104">SYNTAX</span></span>

```
New-AzureAutomationAccount -Name <String> -Location <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="22db7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="22db7-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="22db7-106">Polecenie cmdlet **New-AzureAutomationAccount** tworzy nowe konto w usłudze Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="22db7-106">The **New-AzureAutomationAccount** cmdlet creates a new account in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="22db7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="22db7-107">EXAMPLES</span></span>

### <span data-ttu-id="22db7-108">Przykład 1. Tworzenie konta usługi Automation</span><span class="sxs-lookup"><span data-stu-id="22db7-108">Example 1: Create an Automation account</span></span>
```
PS C:\> New-AzureAutomationAccount -Name "MyAutomationAccount" -Location "East US"
```

<span data-ttu-id="22db7-109">To polecenie tworzy konto usługi Automation o nazwie MyAutomationAccount w regionie wschodnim USA.</span><span class="sxs-lookup"><span data-stu-id="22db7-109">This command creates an Automation account named MyAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="22db7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22db7-110">PARAMETERS</span></span>

### <span data-ttu-id="22db7-111">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="22db7-111">-Location</span></span>
<span data-ttu-id="22db7-112">Określa lokalizację konta.</span><span class="sxs-lookup"><span data-stu-id="22db7-112">Specifies the location of the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22db7-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="22db7-113">-Name</span></span>
<span data-ttu-id="22db7-114">Określa nazwę konta.</span><span class="sxs-lookup"><span data-stu-id="22db7-114">Specifies the name of the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22db7-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="22db7-115">-Profile</span></span>
<span data-ttu-id="22db7-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22db7-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="22db7-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="22db7-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22db7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22db7-118">CommonParameters</span></span>
<span data-ttu-id="22db7-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22db7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22db7-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22db7-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22db7-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22db7-121">INPUTS</span></span>

## <span data-ttu-id="22db7-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="22db7-122">OUTPUTS</span></span>

### <span data-ttu-id="22db7-123">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="22db7-123">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="22db7-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="22db7-124">NOTES</span></span>

## <span data-ttu-id="22db7-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22db7-125">RELATED LINKS</span></span>

[<span data-ttu-id="22db7-126">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="22db7-126">Get-AzureAutomationAccount</span></span>](./Get-AzureAutomationAccount.md)

[<span data-ttu-id="22db7-127">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="22db7-127">Remove-AzureAutomationAccount</span></span>](./Remove-AzureAutomationAccount.md)


