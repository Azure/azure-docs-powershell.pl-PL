---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 7481975d880d3d43508756ac2daec3e665878ee0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710580"
---
# <span data-ttu-id="d9f0b-101">Get-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="d9f0b-101">Get-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="d9f0b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d9f0b-102">SYNOPSIS</span></span>
<span data-ttu-id="d9f0b-103">Pobiera grupy hybrydowych procesów roboczych elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-103">Gets hybrid runbook worker groups.</span></span>

## <span data-ttu-id="d9f0b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d9f0b-104">SYNTAX</span></span>

### <span data-ttu-id="d9f0b-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d9f0b-105">ByAll (Default)</span></span>
```
Get-AzAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9f0b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d9f0b-106">ByName</span></span>
```
Get-AzAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9f0b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d9f0b-107">DESCRIPTION</span></span>
<span data-ttu-id="d9f0b-108">Polecenie cmdlet **Get-AzAutomationHybridWorkerGroup** pobiera hybrydowe grupy procesów roboczych elementu Runbook usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-108">The **Get-AzAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="d9f0b-109">Aby uzyskać określoną grupę, określ jej nazwę.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="d9f0b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d9f0b-110">EXAMPLES</span></span>

### <span data-ttu-id="d9f0b-111">Przykład 1: pobieranie wszystkich grup hybrydowych procesów roboczych Runbook</span><span class="sxs-lookup"><span data-stu-id="d9f0b-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="d9f0b-112">To polecenie pobiera wszystkie grupy hybrydowych procesów roboczych elementu Runbook z konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="d9f0b-113">Przykład 2: uzyskiwanie pojedynczego grupy hybrydowego procesu roboczego elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="d9f0b-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="d9f0b-114">To polecenie uzyskuje grupę hybrydowego procesu roboczego elementu Runbook o nazwie HybridRunbookWorkerGroup01 na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="d9f0b-115">Przykład 3: pobieranie pracowników z grupy hybrydowego procesu roboczego elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="d9f0b-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="d9f0b-116">To polecenie pobiera hybrydowe procesy robocze Runbook z grupy hybrydowego procesu roboczego elementu Runbook o nazwie HybridRunbookWorkerGroup01 na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="d9f0b-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d9f0b-117">PARAMETERS</span></span>

### <span data-ttu-id="d9f0b-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d9f0b-118">-AutomationAccountName</span></span>
<span data-ttu-id="d9f0b-119">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="d9f0b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9f0b-120">-DefaultProfile</span></span>
<span data-ttu-id="d9f0b-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d9f0b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9f0b-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d9f0b-122">-Name</span></span>
<span data-ttu-id="d9f0b-123">Określa nazwę grupy hybrydowego procesu roboczego elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-123">Specifies the hybrid runbook worker group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Group

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9f0b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9f0b-124">-ResourceGroupName</span></span>
<span data-ttu-id="d9f0b-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d9f0b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9f0b-126">CommonParameters</span></span>
<span data-ttu-id="d9f0b-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9f0b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9f0b-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9f0b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9f0b-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9f0b-129">INPUTS</span></span>

### <span data-ttu-id="d9f0b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d9f0b-130">System.String</span></span>

## <span data-ttu-id="d9f0b-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d9f0b-131">OUTPUTS</span></span>

### <span data-ttu-id="d9f0b-132">Microsoft. Azure. Commands. Automation. model. HybridRunbookWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="d9f0b-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span></span>

## <span data-ttu-id="d9f0b-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d9f0b-133">NOTES</span></span>

## <span data-ttu-id="d9f0b-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9f0b-134">RELATED LINKS</span></span>
