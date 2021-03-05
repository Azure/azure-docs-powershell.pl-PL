---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
ms.openlocfilehash: 051eee1c191662e6ca4eb56e34088af651ea69f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014161"
---
# <span data-ttu-id="5f93e-101">Get-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="5f93e-101">Get-AzAutomationSourceControl</span></span>

## <span data-ttu-id="5f93e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f93e-102">SYNOPSIS</span></span>
<span data-ttu-id="5f93e-103">Pobiera listę kontrolek źródeł usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="5f93e-103">Gets a list of Azure Automation source controls.</span></span>

## <span data-ttu-id="5f93e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5f93e-104">SYNTAX</span></span>

### <span data-ttu-id="5f93e-105">ByAll (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="5f93e-105">ByAll (Default)</span></span>
```
Get-AzAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f93e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5f93e-106">ByName</span></span>
```
Get-AzAutomationSourceControl -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f93e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="5f93e-107">DESCRIPTION</span></span>
<span data-ttu-id="5f93e-108">Polecenie Get-AzAutomationSourceControl pobiera kontrolki źródła automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="5f93e-108">The Get-AzAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="5f93e-109">Aby uzyskać określoną kontrolkę źródłową, określ jej nazwę.</span><span class="sxs-lookup"><span data-stu-id="5f93e-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="5f93e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5f93e-110">EXAMPLES</span></span>

### <span data-ttu-id="5f93e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5f93e-111">Example 1</span></span>
<span data-ttu-id="5f93e-112">To polecenie pobiera kontrolkę źródła automatyzacji o nazwie VSTSNative na koncie o nazwie devAccount.</span><span class="sxs-lookup"><span data-stu-id="5f93e-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="5f93e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f93e-113">PARAMETERS</span></span>

### <span data-ttu-id="5f93e-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5f93e-114">-AutomationAccountName</span></span>
<span data-ttu-id="5f93e-115">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="5f93e-115">The automation account name.</span></span>

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

### <span data-ttu-id="5f93e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f93e-116">-DefaultProfile</span></span>
<span data-ttu-id="5f93e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5f93e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f93e-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5f93e-118">-Name</span></span>
<span data-ttu-id="5f93e-119">Nazwa kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="5f93e-119">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f93e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f93e-120">-ResourceGroupName</span></span>
<span data-ttu-id="5f93e-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5f93e-121">The resource group name.</span></span>

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

### <span data-ttu-id="5f93e-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="5f93e-122">-SourceType</span></span>
<span data-ttu-id="5f93e-123">Typ kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="5f93e-123">The source control type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:
Accepted values: GitHub, VsoGit, VsoTfvc

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f93e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f93e-124">CommonParameters</span></span>
<span data-ttu-id="5f93e-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f93e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f93e-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f93e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f93e-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f93e-127">INPUTS</span></span>

### <span data-ttu-id="5f93e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5f93e-128">System.String</span></span>

## <span data-ttu-id="5f93e-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f93e-129">OUTPUTS</span></span>

### <span data-ttu-id="5f93e-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span><span class="sxs-lookup"><span data-stu-id="5f93e-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="5f93e-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5f93e-131">NOTES</span></span>

## <span data-ttu-id="5f93e-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f93e-132">RELATED LINKS</span></span>
