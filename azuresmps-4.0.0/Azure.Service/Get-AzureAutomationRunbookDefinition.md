---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 66740917-E8BB-44ED-9CBB-9825BD1840E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b049d770dbcee8b7cea56dbadbf7d4071c344cc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055328"
---
# <span data-ttu-id="3223c-101">Get-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="3223c-101">Get-AzureAutomationRunbookDefinition</span></span>

## <span data-ttu-id="3223c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3223c-102">SYNOPSIS</span></span>

<span data-ttu-id="3223c-103">Pobiera definicję elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="3223c-103">Gets a runbook definition.</span></span>

## <span data-ttu-id="3223c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3223c-104">SYNTAX</span></span>

```
Get-AzureAutomationRunbookDefinition -Name <String> [-Slot <String>] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3223c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3223c-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="3223c-106">Polecenie cmdlet **Get-AzureAutomationRunbookDefinition** pobiera definicję wersji roboczej, opublikowaną definicję lub obie definicje elementu Runbook usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="3223c-106">The **Get-AzureAutomationRunbookDefinition** cmdlet gets the draft definition, the published definition, or both definitions of an Azure Automation runbook.</span></span>
<span data-ttu-id="3223c-107">Domyślnie jest zwracana opublikowana wersja.</span><span class="sxs-lookup"><span data-stu-id="3223c-107">By default, the published version is returned.</span></span>

## <span data-ttu-id="3223c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3223c-108">EXAMPLES</span></span>

### <span data-ttu-id="3223c-109">Przykład 1: uzyskiwanie definicji elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="3223c-109">Example 1: Get a runbook definition</span></span>
```
PS C:\> Get-AzureAutomationRunbookDefinition -AutomationAccountName "Contoso17" -Name "RunbookDef01" -Slot "Published"
```

<span data-ttu-id="3223c-110">To polecenie pobiera opublikowaną definicję elementu Runbook elementu Runbook o nazwie RunbookDef01 na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3223c-110">This command gets the published runbook definition of the runbook named RunbookDef01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="3223c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3223c-111">PARAMETERS</span></span>

### <span data-ttu-id="3223c-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3223c-112">-AutomationAccountName</span></span>
<span data-ttu-id="3223c-113">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="3223c-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="3223c-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3223c-114">-Name</span></span>
<span data-ttu-id="3223c-115">Określa nazwę elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="3223c-115">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3223c-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="3223c-116">-Profile</span></span>
<span data-ttu-id="3223c-117">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3223c-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3223c-118">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="3223c-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3223c-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="3223c-119">-Slot</span></span>
<span data-ttu-id="3223c-120">Określa gniazdo.</span><span class="sxs-lookup"><span data-stu-id="3223c-120">Specifies the slot.</span></span>
<span data-ttu-id="3223c-121">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3223c-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3223c-122">Propozycje</span><span class="sxs-lookup"><span data-stu-id="3223c-122">Draft</span></span>
- <span data-ttu-id="3223c-123">Podawane</span><span class="sxs-lookup"><span data-stu-id="3223c-123">Published</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3223c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3223c-124">CommonParameters</span></span>
<span data-ttu-id="3223c-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3223c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3223c-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3223c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3223c-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3223c-127">INPUTS</span></span>

## <span data-ttu-id="3223c-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3223c-128">OUTPUTS</span></span>

## <span data-ttu-id="3223c-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3223c-129">NOTES</span></span>

## <span data-ttu-id="3223c-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3223c-130">RELATED LINKS</span></span>

[<span data-ttu-id="3223c-131">Set-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="3223c-131">Set-AzureAutomationRunbookDefinition</span></span>](./Set-AzureAutomationRunbookDefinition.md)


