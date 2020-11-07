---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceManagementGroups.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceManagementGroups.md
ms.openlocfilehash: 55fe1a82d0e54606c04954167aef2c2b90086655
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718135"
---
# <span data-ttu-id="38600-101">Get-AzureRmOperationalInsightsWorkspaceManagementGroups</span><span class="sxs-lookup"><span data-stu-id="38600-101">Get-AzureRmOperationalInsightsWorkspaceManagementGroups</span></span>

## <span data-ttu-id="38600-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="38600-102">SYNOPSIS</span></span>
<span data-ttu-id="38600-103">Umożliwia pobieranie szczegółów dotyczących grup zarządzania połączonych z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="38600-103">Gets details of management groups connected to a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38600-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="38600-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceManagementGroups [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38600-105">Opis</span><span class="sxs-lookup"><span data-stu-id="38600-105">DESCRIPTION</span></span>
<span data-ttu-id="38600-106">Polecenie cmdlet **Get-AzureRmOperationalInsightsWorkspaceManagementGroups** zawiera listę grup zarządzania, które są połączone z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="38600-106">The **Get-AzureRmOperationalInsightsWorkspaceManagementGroups** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="38600-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="38600-107">EXAMPLES</span></span>

### <span data-ttu-id="38600-108">Przykład 1: Uzyskaj grupy zarządzania według nazwy obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="38600-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceManagementGroups -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="38600-109">To polecenie umożliwia pobieranie grup zarządzania dla obszaru roboczego o nazwie Moja przestrzeń robocza w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="38600-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="38600-110">Przykład 2: uzyskiwanie grup zarządzania przy użyciu rurociągu</span><span class="sxs-lookup"><span data-stu-id="38600-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureOperationalInsightsWorkspaceManagementGroups
```

<span data-ttu-id="38600-111">To polecenie używa polecenia cmdlet Get-AzureRmOperationalInsightsWorkspace, aby uzyskać obszar roboczy o nazwie webworkspace, a następnie przekazywać obszar roboczy do bieżącego polecenia cmdlet, który pobiera grupy zarządzania dla tego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="38600-111">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="38600-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="38600-112">PARAMETERS</span></span>

### <span data-ttu-id="38600-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="38600-113">-Name</span></span>
<span data-ttu-id="38600-114">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="38600-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="38600-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38600-115">-ResourceGroupName</span></span>
<span data-ttu-id="38600-116">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="38600-116">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="38600-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38600-117">-DefaultProfile</span></span>
<span data-ttu-id="38600-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="38600-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38600-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38600-119">CommonParameters</span></span>
<span data-ttu-id="38600-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38600-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38600-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38600-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38600-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38600-122">INPUTS</span></span>

## <span data-ttu-id="38600-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="38600-123">OUTPUTS</span></span>

### <span data-ttu-id="38600-124">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. OperationalInsights. modele. PSManagementGroup]</span><span class="sxs-lookup"><span data-stu-id="38600-124">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup]</span></span>

## <span data-ttu-id="38600-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="38600-125">NOTES</span></span>

## <span data-ttu-id="38600-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38600-126">RELATED LINKS</span></span>

[<span data-ttu-id="38600-127">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="38600-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="38600-128">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="38600-128">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)

