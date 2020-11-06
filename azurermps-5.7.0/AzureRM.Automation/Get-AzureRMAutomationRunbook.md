---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
ms.openlocfilehash: d9ffd6ae2f7695a02f8c29fbe745202642039af6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553697"
---
# <span data-ttu-id="9fbee-101">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9fbee-101">Get-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="9fbee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9fbee-102">SYNOPSIS</span></span>
<span data-ttu-id="9fbee-103">Pobiera element Runbook.</span><span class="sxs-lookup"><span data-stu-id="9fbee-103">Gets a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fbee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9fbee-104">SYNTAX</span></span>

### <span data-ttu-id="9fbee-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9fbee-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fbee-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="9fbee-106">ByRunbookName</span></span>
```
Get-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fbee-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9fbee-107">DESCRIPTION</span></span>
<span data-ttu-id="9fbee-108">Polecenie cmdlet **Get-AzureRmAutomationRunbook** Pobiera elementy Runbook usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="9fbee-108">The **Get-AzureRmAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="9fbee-109">Aby uzyskać określony element Runbook, określ jego nazwę.</span><span class="sxs-lookup"><span data-stu-id="9fbee-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="9fbee-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9fbee-110">EXAMPLES</span></span>

### <span data-ttu-id="9fbee-111">Przykład 1. pobieranie wszystkich elementów Runbook</span><span class="sxs-lookup"><span data-stu-id="9fbee-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9fbee-112">To polecenie pobiera wszystkie elementy Runbook z konta usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9fbee-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="9fbee-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9fbee-113">PARAMETERS</span></span>

### <span data-ttu-id="9fbee-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9fbee-114">-AutomationAccountName</span></span>
<span data-ttu-id="9fbee-115">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet pobiera elementy Runbook.</span><span class="sxs-lookup"><span data-stu-id="9fbee-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fbee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fbee-116">-DefaultProfile</span></span>
<span data-ttu-id="9fbee-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9fbee-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fbee-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9fbee-118">-Name</span></span>
<span data-ttu-id="9fbee-119">Określa nazwę elementu Runbook, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fbee-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fbee-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fbee-120">-ResourceGroupName</span></span>
<span data-ttu-id="9fbee-121">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera elementy Runbook.</span><span class="sxs-lookup"><span data-stu-id="9fbee-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fbee-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fbee-122">CommonParameters</span></span>
<span data-ttu-id="9fbee-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fbee-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fbee-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fbee-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fbee-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9fbee-125">INPUTS</span></span>

### <span data-ttu-id="9fbee-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9fbee-126">None</span></span>
<span data-ttu-id="9fbee-127">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="9fbee-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9fbee-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9fbee-128">OUTPUTS</span></span>

### <span data-ttu-id="9fbee-129">Microsoft. Azure. Commands. Automation. model. Runbook</span><span class="sxs-lookup"><span data-stu-id="9fbee-129">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="9fbee-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9fbee-130">NOTES</span></span>

## <span data-ttu-id="9fbee-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9fbee-131">RELATED LINKS</span></span>

[<span data-ttu-id="9fbee-132">Eksportowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9fbee-132">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9fbee-133">Import — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9fbee-133">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9fbee-134">Nowe — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9fbee-134">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9fbee-135">Nowe — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9fbee-135">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9fbee-136">Publikowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9fbee-136">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9fbee-137">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9fbee-137">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9fbee-138">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9fbee-138">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9fbee-139">Start — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9fbee-139">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


