---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 7B2D9768-919B-4F54-BBC7-8882CC2C973A
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9ce55e573881a29291085e9bf25381170bbf052
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055337"
---
# <span data-ttu-id="c438f-101">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="c438f-101">Get-AzureAutomationAccount</span></span>

## <span data-ttu-id="c438f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c438f-102">SYNOPSIS</span></span>

<span data-ttu-id="c438f-103">Pobiera konta usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c438f-103">Gets Azure Automation accounts.</span></span>

## <span data-ttu-id="c438f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c438f-104">SYNTAX</span></span>

```
Get-AzureAutomationAccount [-Name <String>] [-Location <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c438f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c438f-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="c438f-106">Polecenie cmdlet **Get-AzureAutomationAccount** pobiera konta usługi Microsoft Azure Automation dla Twojej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c438f-106">The **Get-AzureAutomationAccount** cmdlet gets the Microsoft Azure Automation accounts for your subscription.</span></span>
<span data-ttu-id="c438f-107">Konto usługi Automation to kontener zasobów automatyzacji odizolowanych od zasobów innych kont automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="c438f-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span>
<span data-ttu-id="c438f-108">Zasoby automatyzacji obejmują elementy Runbook, zadania i zasoby.</span><span class="sxs-lookup"><span data-stu-id="c438f-108">Automation resources include runbooks, jobs, and assets.</span></span>

## <span data-ttu-id="c438f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c438f-109">EXAMPLES</span></span>

### <span data-ttu-id="c438f-110">Przykład 1: Uzyskiwanie konta usługi Automation</span><span class="sxs-lookup"><span data-stu-id="c438f-110">Example 1: Get an Automation account</span></span>
```
PS C:\> Get-AzureAutomationAccount -Name "Contoso17"
```

<span data-ttu-id="c438f-111">To polecenie uzyskuje konto usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c438f-111">This command gets the Automation account named Contoso17.</span></span>

## <span data-ttu-id="c438f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c438f-112">PARAMETERS</span></span>

### <span data-ttu-id="c438f-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c438f-113">-Location</span></span>
<span data-ttu-id="c438f-114">Określa lokalizację platformy Azure skojarzoną z kontami automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="c438f-114">Specifies an Azure location associated with Automation accounts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c438f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c438f-115">-Name</span></span>
<span data-ttu-id="c438f-116">Określa nazwę konta usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c438f-116">Specifies the name of an Azure Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c438f-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="c438f-117">-Profile</span></span>
<span data-ttu-id="c438f-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c438f-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c438f-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="c438f-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c438f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c438f-120">CommonParameters</span></span>
<span data-ttu-id="c438f-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c438f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c438f-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c438f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c438f-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c438f-123">INPUTS</span></span>

## <span data-ttu-id="c438f-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c438f-124">OUTPUTS</span></span>

### <span data-ttu-id="c438f-125">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="c438f-125">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="c438f-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c438f-126">NOTES</span></span>

## <span data-ttu-id="c438f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c438f-127">RELATED LINKS</span></span>

[<span data-ttu-id="c438f-128">Nowe — AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="c438f-128">New-AzureAutomationAccount</span></span>](./New-AzureAutomationAccount.md)

[<span data-ttu-id="c438f-129">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="c438f-129">Remove-AzureAutomationAccount</span></span>](./Remove-AzureAutomationAccount.md)


