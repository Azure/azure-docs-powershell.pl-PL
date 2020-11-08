---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 0B496085-670D-45F7-B989-D4541A3811FF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37d95c570cc1c12bc40704ec2a2d89fcbec7cf48
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054900"
---
# <span data-ttu-id="00906-101">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="00906-101">New-AzureAutomationRunbook</span></span>

## <span data-ttu-id="00906-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="00906-102">SYNOPSIS</span></span>

<span data-ttu-id="00906-103">Tworzy element Runbook.</span><span class="sxs-lookup"><span data-stu-id="00906-103">Creates a runbook.</span></span>

## <span data-ttu-id="00906-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="00906-104">SYNTAX</span></span>

### <span data-ttu-id="00906-105">ByRunbookName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="00906-105">ByRunbookName (Default)</span></span>
```
New-AzureAutomationRunbook -Name <String> [-Description <String>] [-Tags <String[]>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="00906-106">ByPath</span><span class="sxs-lookup"><span data-stu-id="00906-106">ByPath</span></span>
```
New-AzureAutomationRunbook -Path <String> [-Description <String>] [-Tags <String[]>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="00906-107">Opis</span><span class="sxs-lookup"><span data-stu-id="00906-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="00906-108">Polecenie cmdlet **New-AzureAutomationRunbook** tworzy nowy, pusty element Runbook usługi Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="00906-108">The **New-AzureAutomationRunbook** cmdlet creates a new, empty Microsoft Azure Automation runbook.</span></span>
<span data-ttu-id="00906-109">Określ nazwę, aby utworzyć nowy element Runbook.</span><span class="sxs-lookup"><span data-stu-id="00906-109">Specify a name to create a new runbook.</span></span>

<span data-ttu-id="00906-110">Możesz również określić ścieżkę do pliku skryptu programu Windows PowerShell (ps1), aby zaimportować element Runbook.</span><span class="sxs-lookup"><span data-stu-id="00906-110">You can also specify the path to a Windows PowerShell script (.ps1 ) file to import a runbook.</span></span>
<span data-ttu-id="00906-111">Skrypt do zaimportowania musi zawierać pojedynczą definicję przepływu pracy programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="00906-111">The script to import must contain a single Windows PowerShell Workflow definition.</span></span>
<span data-ttu-id="00906-112">Nazwa tego przepływu pracy programu Windows PowerShell stanie się nazwą elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="00906-112">The name of this Windows PowerShell Workflow becomes the name of the runbook.</span></span>

## <span data-ttu-id="00906-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="00906-113">EXAMPLES</span></span>

### <span data-ttu-id="00906-114">Przykład 1. Tworzenie elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="00906-114">Example 1: Create a runbook</span></span>
```
PS C:\> New-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02"
```

<span data-ttu-id="00906-115">To polecenie tworzy nowy element Runbook o nazwie Runbook02 na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="00906-115">This command creates a new runbook named Runbook02 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="00906-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="00906-116">PARAMETERS</span></span>

### <span data-ttu-id="00906-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="00906-117">-AutomationAccountName</span></span>
<span data-ttu-id="00906-118">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="00906-118">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="00906-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="00906-119">-Description</span></span>
<span data-ttu-id="00906-120">Określa opis elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="00906-120">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="00906-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="00906-121">-Name</span></span>
<span data-ttu-id="00906-122">Określa nazwę elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="00906-122">Specifies the name for the runbook.</span></span>

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

### <span data-ttu-id="00906-123">-Path</span><span class="sxs-lookup"><span data-stu-id="00906-123">-Path</span></span>
<span data-ttu-id="00906-124">Określa ścieżkę.</span><span class="sxs-lookup"><span data-stu-id="00906-124">Specifies the path.</span></span>

```yaml
Type: String
Parameter Sets: ByPath
Aliases: RunbookPath

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00906-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="00906-125">-Profile</span></span>
<span data-ttu-id="00906-126">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00906-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="00906-127">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="00906-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="00906-128">-Tagi</span><span class="sxs-lookup"><span data-stu-id="00906-128">-Tags</span></span>
<span data-ttu-id="00906-129">Określa Tagi elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="00906-129">Specifies tags for the runbook.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00906-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00906-130">CommonParameters</span></span>
<span data-ttu-id="00906-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00906-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00906-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00906-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00906-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00906-133">INPUTS</span></span>

## <span data-ttu-id="00906-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="00906-134">OUTPUTS</span></span>

### <span data-ttu-id="00906-135">Microsoft. Azure. Commands. Automation. model. Runbook</span><span class="sxs-lookup"><span data-stu-id="00906-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="00906-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="00906-136">NOTES</span></span>

## <span data-ttu-id="00906-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00906-137">RELATED LINKS</span></span>

[<span data-ttu-id="00906-138">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="00906-138">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="00906-139">Publikowanie — AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="00906-139">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="00906-140">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="00906-140">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="00906-141">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="00906-141">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="00906-142">Start — AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="00906-142">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


