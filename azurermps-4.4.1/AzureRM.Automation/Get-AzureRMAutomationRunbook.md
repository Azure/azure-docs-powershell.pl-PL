---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
ms.openlocfilehash: e543a7da3ce5502e0f78619ca4fbb455b29b82d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527741"
---
# <span data-ttu-id="49a07-101">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="49a07-101">Get-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="49a07-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="49a07-102">SYNOPSIS</span></span>
<span data-ttu-id="49a07-103">Pobiera element Runbook.</span><span class="sxs-lookup"><span data-stu-id="49a07-103">Gets a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49a07-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="49a07-104">SYNTAX</span></span>

### <span data-ttu-id="49a07-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="49a07-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49a07-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="49a07-106">ByRunbookName</span></span>
```
Get-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49a07-107">Opis</span><span class="sxs-lookup"><span data-stu-id="49a07-107">DESCRIPTION</span></span>
<span data-ttu-id="49a07-108">Polecenie cmdlet **Get-AzureRmAutomationRunbook** Pobiera elementy Runbook usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="49a07-108">The **Get-AzureRmAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="49a07-109">Aby uzyskać określony element Runbook, określ jego nazwę.</span><span class="sxs-lookup"><span data-stu-id="49a07-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="49a07-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="49a07-110">EXAMPLES</span></span>

### <span data-ttu-id="49a07-111">Przykład 1. pobieranie wszystkich elementów Runbook</span><span class="sxs-lookup"><span data-stu-id="49a07-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="49a07-112">To polecenie pobiera wszystkie elementy Runbook z konta usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="49a07-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="49a07-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="49a07-113">PARAMETERS</span></span>

### <span data-ttu-id="49a07-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="49a07-114">-AutomationAccountName</span></span>
<span data-ttu-id="49a07-115">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet pobiera elementy Runbook.</span><span class="sxs-lookup"><span data-stu-id="49a07-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49a07-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="49a07-116">-Name</span></span>
<span data-ttu-id="49a07-117">Określa nazwę elementu Runbook, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49a07-117">Specifies the name of a runbook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49a07-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49a07-118">-ResourceGroupName</span></span>
<span data-ttu-id="49a07-119">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera elementy Runbook.</span><span class="sxs-lookup"><span data-stu-id="49a07-119">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49a07-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49a07-120">-DefaultProfile</span></span>
<span data-ttu-id="49a07-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="49a07-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a07-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49a07-122">CommonParameters</span></span>
<span data-ttu-id="49a07-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49a07-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49a07-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49a07-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49a07-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49a07-125">INPUTS</span></span>

## <span data-ttu-id="49a07-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="49a07-126">OUTPUTS</span></span>

### <span data-ttu-id="49a07-127">Microsoft. Azure. Commands. Automation. model. Runbook</span><span class="sxs-lookup"><span data-stu-id="49a07-127">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="49a07-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="49a07-128">NOTES</span></span>

## <span data-ttu-id="49a07-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49a07-129">RELATED LINKS</span></span>

[<span data-ttu-id="49a07-130">Eksportowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="49a07-130">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="49a07-131">Import — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="49a07-131">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="49a07-132">Nowe — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="49a07-132">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="49a07-133">Nowe — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="49a07-133">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="49a07-134">Publikowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="49a07-134">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="49a07-135">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="49a07-135">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="49a07-136">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="49a07-136">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="49a07-137">Start — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="49a07-137">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


