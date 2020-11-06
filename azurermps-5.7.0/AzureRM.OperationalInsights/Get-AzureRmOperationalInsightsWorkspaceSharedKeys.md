---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspacesharedkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
ms.openlocfilehash: 5fab6a3a0419047fef32f5bf32f52e1f7ee57d3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528006"
---
# <span data-ttu-id="01060-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span><span class="sxs-lookup"><span data-stu-id="01060-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span></span>

## <span data-ttu-id="01060-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="01060-102">SYNOPSIS</span></span>
<span data-ttu-id="01060-103">Pobiera klucze współużytkowane dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="01060-103">Gets the shared keys for a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01060-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="01060-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceSharedKeys [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01060-105">Opis</span><span class="sxs-lookup"><span data-stu-id="01060-105">DESCRIPTION</span></span>
<span data-ttu-id="01060-106">Polecenie cmdlet **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** zawiera listę kluczy współużytkowanych dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="01060-106">The **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="01060-107">Klucze służą do łączenia agentów usługi Insights z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="01060-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="01060-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="01060-108">EXAMPLES</span></span>

### <span data-ttu-id="01060-109">Przykład 1: pobieranie kluczy współużytkowanych według nazwy obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="01060-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceSharedKeys -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="01060-110">To polecenie pobiera klucze udostępnione dla obszaru roboczego o nazwie Moja przestrzeń robocza w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="01060-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="01060-111">Przykład 2: pobieranie kluczy współużytkowanych za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="01060-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureRmOperationalInsightsWorkspaceSharedKeys
```

<span data-ttu-id="01060-112">To polecenie pobiera obszar roboczy o nazwie webworkspace za pomocą polecenia cmdlet Get-AzureRmOperationalInsightsWorkspace, a następnie przekazuje obszar roboczy do polecenia cmdlet **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** .</span><span class="sxs-lookup"><span data-stu-id="01060-112">This command gets the workspace named MyWorkspace using the Get-AzureRmOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet.</span></span>
<span data-ttu-id="01060-113">Polecenie pobiera klucze współużytkowane dla tego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="01060-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="01060-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="01060-114">PARAMETERS</span></span>

### <span data-ttu-id="01060-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01060-115">-DefaultProfile</span></span>
<span data-ttu-id="01060-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="01060-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01060-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="01060-117">-Name</span></span>
<span data-ttu-id="01060-118">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="01060-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="01060-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01060-119">-ResourceGroupName</span></span>
<span data-ttu-id="01060-120">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="01060-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="01060-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01060-121">CommonParameters</span></span>
<span data-ttu-id="01060-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01060-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01060-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01060-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01060-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01060-124">INPUTS</span></span>

### <span data-ttu-id="01060-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="01060-125">None</span></span>
<span data-ttu-id="01060-126">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="01060-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="01060-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="01060-127">OUTPUTS</span></span>

### <span data-ttu-id="01060-128">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="01060-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="01060-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="01060-129">NOTES</span></span>

## <span data-ttu-id="01060-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01060-130">RELATED LINKS</span></span>

[<span data-ttu-id="01060-131">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="01060-131">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="01060-132">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="01060-132">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


