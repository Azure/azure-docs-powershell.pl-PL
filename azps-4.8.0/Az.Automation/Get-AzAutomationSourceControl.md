---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
ms.openlocfilehash: 42472efdde4ccf96f12a0617d9a86175eed13d1c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221610"
---
# <span data-ttu-id="d6cde-101">Get-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="d6cde-101">Get-AzAutomationSourceControl</span></span>

## <span data-ttu-id="d6cde-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d6cde-102">SYNOPSIS</span></span>
<span data-ttu-id="d6cde-103">Pobiera listę kontrolek źródłowych usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d6cde-103">Gets a list of Azure Automation source controls.</span></span>

## <span data-ttu-id="d6cde-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d6cde-104">SYNTAX</span></span>

### <span data-ttu-id="d6cde-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d6cde-105">ByAll (Default)</span></span>
```
Get-AzAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6cde-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d6cde-106">ByName</span></span>
```
Get-AzAutomationSourceControl -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6cde-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d6cde-107">DESCRIPTION</span></span>
<span data-ttu-id="d6cde-108">Polecenie cmdlet Get-AzAutomationSourceControl umożliwia pobieranie kontrolek źródeł automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="d6cde-108">The Get-AzAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="d6cde-109">Aby uzyskać określoną kontrolę źródła, określ jej nazwę.</span><span class="sxs-lookup"><span data-stu-id="d6cde-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="d6cde-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d6cde-110">EXAMPLES</span></span>

### <span data-ttu-id="d6cde-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d6cde-111">Example 1</span></span>
<span data-ttu-id="d6cde-112">To polecenie pobiera kontrolę źródła automatyzacji o nazwie VSTSNative na koncie o nazwie devAccount.</span><span class="sxs-lookup"><span data-stu-id="d6cde-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="d6cde-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d6cde-113">PARAMETERS</span></span>

### <span data-ttu-id="d6cde-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d6cde-114">-AutomationAccountName</span></span>
<span data-ttu-id="d6cde-115">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="d6cde-115">The automation account name.</span></span>

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

### <span data-ttu-id="d6cde-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6cde-116">-DefaultProfile</span></span>
<span data-ttu-id="d6cde-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6cde-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6cde-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d6cde-118">-Name</span></span>
<span data-ttu-id="d6cde-119">Nazwa kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="d6cde-119">The source control name.</span></span>

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

### <span data-ttu-id="d6cde-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6cde-120">-ResourceGroupName</span></span>
<span data-ttu-id="d6cde-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d6cde-121">The resource group name.</span></span>

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

### <span data-ttu-id="d6cde-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="d6cde-122">-SourceType</span></span>
<span data-ttu-id="d6cde-123">Typ kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="d6cde-123">The source control type.</span></span>

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

### <span data-ttu-id="d6cde-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6cde-124">CommonParameters</span></span>
<span data-ttu-id="d6cde-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6cde-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6cde-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6cde-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6cde-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6cde-127">INPUTS</span></span>

### <span data-ttu-id="d6cde-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d6cde-128">System.String</span></span>

## <span data-ttu-id="d6cde-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d6cde-129">OUTPUTS</span></span>

### <span data-ttu-id="d6cde-130">Microsoft. Azure. Commands. Automation. model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="d6cde-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="d6cde-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d6cde-131">NOTES</span></span>

## <span data-ttu-id="d6cde-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6cde-132">RELATED LINKS</span></span>
