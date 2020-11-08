---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C24CFC83-3151-452D-A7B9-E78466493474
online version: ''
schema: 2.0.0
ms.openlocfilehash: e193dba6f64553e5e52d7f900bdc5c54deac5112
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055038"
---
# <span data-ttu-id="08191-101">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="08191-101">Set-AzureAutomationRunbook</span></span>

## <span data-ttu-id="08191-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08191-102">SYNOPSIS</span></span>

<span data-ttu-id="08191-103">Modyfikuje konfigurację elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="08191-103">Modifies the configuration of a runbook.</span></span>

## <span data-ttu-id="08191-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08191-104">SYNTAX</span></span>

```
Set-AzureAutomationRunbook -Name <String> [-Description <String>] [-Tags <String[]>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="08191-105">Opis</span><span class="sxs-lookup"><span data-stu-id="08191-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="08191-106">Polecenie cmdlet **Set-AzureAutomationRunbook** modyfikuje konfigurację elementu Runbook usługi Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="08191-106">The **Set-AzureAutomationRunbook** cmdlet modifies the configuration of a Microsoft Azure Automation runbook.</span></span>

## <span data-ttu-id="08191-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08191-107">EXAMPLES</span></span>

### <span data-ttu-id="08191-108">Przykład 1: Włączanie pełnego rejestrowania elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="08191-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\> Set-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "MyRunbook" -LogVerbose $True
```

<span data-ttu-id="08191-109">To polecenie umożliwia pełne rejestrowanie zadań określonego elementu Runbook w koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="08191-109">This command enables verbose logging for the jobs of the specified runbook in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="08191-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08191-110">PARAMETERS</span></span>

### <span data-ttu-id="08191-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="08191-111">-AutomationAccountName</span></span>
<span data-ttu-id="08191-112">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="08191-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="08191-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="08191-113">-Description</span></span>
<span data-ttu-id="08191-114">Określa opis elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="08191-114">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="08191-115">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="08191-115">-LogProgress</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08191-116">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="08191-116">-LogVerbose</span></span>
<span data-ttu-id="08191-117">Wskazuje, czy ma być używane pełne rejestrowanie.</span><span class="sxs-lookup"><span data-stu-id="08191-117">Indicates whether to use verbose logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08191-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="08191-118">-Name</span></span>
<span data-ttu-id="08191-119">Określa nazwę.</span><span class="sxs-lookup"><span data-stu-id="08191-119">Specifies a name.</span></span>

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

### <span data-ttu-id="08191-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="08191-120">-Profile</span></span>
<span data-ttu-id="08191-121">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08191-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="08191-122">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="08191-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="08191-123">-Tagi</span><span class="sxs-lookup"><span data-stu-id="08191-123">-Tags</span></span>
<span data-ttu-id="08191-124">Określa tablicę znaczników.</span><span class="sxs-lookup"><span data-stu-id="08191-124">Specifies an array of tags.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08191-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08191-125">CommonParameters</span></span>
<span data-ttu-id="08191-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08191-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08191-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08191-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08191-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08191-128">INPUTS</span></span>

## <span data-ttu-id="08191-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08191-129">OUTPUTS</span></span>

### <span data-ttu-id="08191-130">Microsoft. Azure. Commands. Automation. model. Runbook</span><span class="sxs-lookup"><span data-stu-id="08191-130">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="08191-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08191-131">NOTES</span></span>

## <span data-ttu-id="08191-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08191-132">RELATED LINKS</span></span>

[<span data-ttu-id="08191-133">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="08191-133">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="08191-134">Nowe — AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="08191-134">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="08191-135">Publikowanie — AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="08191-135">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="08191-136">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="08191-136">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="08191-137">Start — AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="08191-137">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


