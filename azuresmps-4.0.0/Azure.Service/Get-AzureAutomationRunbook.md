---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 304F71E0-9E89-46E6-BD25-7584601CC845
online version: ''
schema: 2.0.0
ms.openlocfilehash: e507b1b35bf8739c80bbdf92f02f29099ceb3284
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054623"
---
# <span data-ttu-id="20cc6-101">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="20cc6-101">Get-AzureAutomationRunbook</span></span>

## <span data-ttu-id="20cc6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="20cc6-102">SYNOPSIS</span></span>

<span data-ttu-id="20cc6-103">Pobiera element Runbook.</span><span class="sxs-lookup"><span data-stu-id="20cc6-103">Gets a runbook.</span></span>

## <span data-ttu-id="20cc6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="20cc6-104">SYNTAX</span></span>

### <span data-ttu-id="20cc6-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="20cc6-105">ByAll (Default)</span></span>
```
Get-AzureAutomationRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="20cc6-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="20cc6-106">ByRunbookName</span></span>
```
Get-AzureAutomationRunbook -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="20cc6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="20cc6-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="20cc6-108">Polecenie cmdlet **Get-AzureAutomationRunbook** pobiera co najmniej jeden element Runbook usługi Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="20cc6-108">The **Get-AzureAutomationRunbook** cmdlet gets one or more Microsoft Azure Automation runbooks.</span></span>
<span data-ttu-id="20cc6-109">Domyślnie zostaną zwrócone wszystkie elementy Runbook.</span><span class="sxs-lookup"><span data-stu-id="20cc6-109">By default, all runbooks are returned.</span></span>
<span data-ttu-id="20cc6-110">Aby uzyskać określony element Runbook, określ jego nazwę lub identyfikator.</span><span class="sxs-lookup"><span data-stu-id="20cc6-110">To get a specific runbook, specify its name or ID.</span></span>
<span data-ttu-id="20cc6-111">Aby uzyskać dostęp do wszystkich elementów Runbook połączonych z określonym harmonogramem, określ nazwę harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="20cc6-111">To get all runbooks linked to a specific schedule, specify the schedule name.</span></span>

## <span data-ttu-id="20cc6-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="20cc6-112">EXAMPLES</span></span>

### <span data-ttu-id="20cc6-113">Przykład 1. pobieranie wszystkich elementów Runbook</span><span class="sxs-lookup"><span data-stu-id="20cc6-113">Example 1: Get all runbooks</span></span>
```
PS C:\> Get-AzureAutomationRunbook -AutomationAccountName "Contoso17"
```

<span data-ttu-id="20cc6-114">To polecenie pobiera wszystkie elementy Runbook z konta usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="20cc6-114">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="20cc6-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20cc6-115">PARAMETERS</span></span>

### <span data-ttu-id="20cc6-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="20cc6-116">-AutomationAccountName</span></span>
<span data-ttu-id="20cc6-117">Określa nazwę konta usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="20cc6-117">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="20cc6-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="20cc6-118">-Name</span></span>
<span data-ttu-id="20cc6-119">Określa nazwę elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="20cc6-119">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20cc6-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="20cc6-120">-Profile</span></span>
<span data-ttu-id="20cc6-121">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20cc6-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="20cc6-122">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="20cc6-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="20cc6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20cc6-123">CommonParameters</span></span>
<span data-ttu-id="20cc6-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20cc6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20cc6-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20cc6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20cc6-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20cc6-126">INPUTS</span></span>

## <span data-ttu-id="20cc6-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="20cc6-127">OUTPUTS</span></span>

### <span data-ttu-id="20cc6-128">Microsoft. Azure. Commands. Automation. model. Runbook</span><span class="sxs-lookup"><span data-stu-id="20cc6-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="20cc6-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="20cc6-129">NOTES</span></span>

## <span data-ttu-id="20cc6-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20cc6-130">RELATED LINKS</span></span>

[<span data-ttu-id="20cc6-131">Nowe — AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="20cc6-131">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="20cc6-132">Publikowanie — AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="20cc6-132">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="20cc6-133">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="20cc6-133">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="20cc6-134">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="20cc6-134">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="20cc6-135">Start — AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="20cc6-135">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


