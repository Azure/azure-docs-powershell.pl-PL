---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B0AE1969-71FD-4B6E-B0C0-1B744814BD5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93dc73193c300f0f10fd9dccaff1c1f3954b8306
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054998"
---
# <span data-ttu-id="5fcd1-101">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5fcd1-101">Start-AzureAutomationRunbook</span></span>

## <span data-ttu-id="5fcd1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5fcd1-102">SYNOPSIS</span></span>

<span data-ttu-id="5fcd1-103">Rozpoczyna zadanie elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-103">Starts a runbook job.</span></span>

## <span data-ttu-id="5fcd1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5fcd1-104">SYNTAX</span></span>

```
Start-AzureAutomationRunbook -Name <String> [-Parameters <IDictionary>] [-RunOn <String>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5fcd1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5fcd1-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="5fcd1-106">Polecenie cmdlet **Start-AzureAutomationRunbook** uruchamia zadanie Runbook usługi Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-106">The **Start-AzureAutomationRunbook** cmdlet starts a Microsoft Azure Automation runbook job.</span></span>
<span data-ttu-id="5fcd1-107">Określ identyfikator lub nazwę elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-107">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="5fcd1-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5fcd1-108">EXAMPLES</span></span>

### <span data-ttu-id="5fcd1-109">Przykład 1. Rozpocznij zadanie elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="5fcd1-109">Example 1: Start a runbook job</span></span>
```
PS C:\> Start-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01"
```

<span data-ttu-id="5fcd1-110">To polecenie uruchamia zadanie w usłudze Runbook dla elementu Runbook o nazwie Runbk01 na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-110">This command starts a runbook job for the runbook named Runbk01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="5fcd1-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5fcd1-111">PARAMETERS</span></span>

### <span data-ttu-id="5fcd1-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5fcd1-112">-AutomationAccountName</span></span>
<span data-ttu-id="5fcd1-113">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="5fcd1-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5fcd1-114">-Name</span></span>
<span data-ttu-id="5fcd1-115">Określa nazwę elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-115">Specifies the name of a runbook.</span></span>

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

### <span data-ttu-id="5fcd1-116">— Parametry</span><span class="sxs-lookup"><span data-stu-id="5fcd1-116">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fcd1-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="5fcd1-117">-Profile</span></span>
<span data-ttu-id="5fcd1-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5fcd1-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5fcd1-120">-RunOn</span><span class="sxs-lookup"><span data-stu-id="5fcd1-120">-RunOn</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fcd1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fcd1-121">CommonParameters</span></span>
<span data-ttu-id="5fcd1-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fcd1-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fcd1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fcd1-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5fcd1-124">INPUTS</span></span>

## <span data-ttu-id="5fcd1-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5fcd1-125">OUTPUTS</span></span>

### <span data-ttu-id="5fcd1-126">Microsoft. Azure. Commands. Automation. model. job</span><span class="sxs-lookup"><span data-stu-id="5fcd1-126">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="5fcd1-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5fcd1-127">NOTES</span></span>

## <span data-ttu-id="5fcd1-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5fcd1-128">RELATED LINKS</span></span>

[<span data-ttu-id="5fcd1-129">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5fcd1-129">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="5fcd1-130">Nowe — AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5fcd1-130">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="5fcd1-131">Publikowanie — AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5fcd1-131">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="5fcd1-132">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5fcd1-132">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="5fcd1-133">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5fcd1-133">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)


