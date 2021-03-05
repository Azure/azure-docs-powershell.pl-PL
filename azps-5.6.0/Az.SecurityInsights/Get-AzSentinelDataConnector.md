---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
ms.openlocfilehash: b99ad26ddfa0239f073c4179413b2f1fefec4d1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986448"
---
# <span data-ttu-id="77b5f-101">Get-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="77b5f-101">Get-AzSentinelDataConnector</span></span>

## <span data-ttu-id="77b5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77b5f-102">SYNOPSIS</span></span>
<span data-ttu-id="77b5f-103">Uzyskiwanie łącznika danych.</span><span class="sxs-lookup"><span data-stu-id="77b5f-103">Get a Data Connector.</span></span>

## <span data-ttu-id="77b5f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="77b5f-104">SYNTAX</span></span>

### <span data-ttu-id="77b5f-105">WorkspaceScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="77b5f-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77b5f-106">DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="77b5f-106">DataConnectorId</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77b5f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="77b5f-107">ResourceId</span></span>
```
Get-AzSentinelDataConnector -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="77b5f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="77b5f-108">DESCRIPTION</span></span>
<span data-ttu-id="77b5f-109">Polecenie **cmdlet Get-AzSentinelDataConnector** pobiera łącznik danych z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="77b5f-109">The **Get-AzSentinelDataConnector** cmdlet gets a Data Connector from the specified workspace.</span></span>
<span data-ttu-id="77b5f-110">Jeśli parametr *DataConnectorId zostanie* określony, zwracany jest jeden obiekt **DataConnector.**</span><span class="sxs-lookup"><span data-stu-id="77b5f-110">If you specify the *DataConnectorId* parameter, a single **DataConnector** object is returned.</span></span>
<span data-ttu-id="77b5f-111">Jeśli parametr *DataConnectorId nie zostanie* określony, zostanie zwrócona tablica zawierająca wszystkie łączniki danych w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="77b5f-111">If you do not specify the *DataConnectorId* parameter, an array containing all of the Data Connectors in the specified workspace are returned.</span></span>
<span data-ttu-id="77b5f-112">Za pomocą obiektu **DataConnector** można na przykład wyłączyć łącznik **danych.**</span><span class="sxs-lookup"><span data-stu-id="77b5f-112">You can use the **DataConnector** object to update the Data Connector, for example you can disable the **DataConnector**.</span></span>

## <span data-ttu-id="77b5f-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="77b5f-113">EXAMPLES</span></span>

### <span data-ttu-id="77b5f-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="77b5f-114">Example 1</span></span>
```powershell
PS C:\> $DataConnectors = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="77b5f-115">W tym przykładzie wszystkie połączenia danych są **przechowywane** w określonym obszarze roboczym, a następnie przechowywane w $DataConnectors danych.</span><span class="sxs-lookup"><span data-stu-id="77b5f-115">This example gets all of the **DataConnectors** in the specified workspace, and then stores it in the $DataConnectors variable.</span></span>

### <span data-ttu-id="77b5f-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="77b5f-116">Example 2</span></span>
```powershell
PS C:\> $DataConnector = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="77b5f-117">Ten przykład pobiera **program DataConnector** w określonym obszarze roboczym, a następnie zapisuje go w $DataConnector danych.</span><span class="sxs-lookup"><span data-stu-id="77b5f-117">This example gets an **DataConnector** in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="77b5f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77b5f-118">PARAMETERS</span></span>

### <span data-ttu-id="77b5f-119">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="77b5f-119">-DataConnectorId</span></span>
<span data-ttu-id="77b5f-120">Identyfikator łącznika danych.</span><span class="sxs-lookup"><span data-stu-id="77b5f-120">Data Connector Id.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b5f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77b5f-121">-DefaultProfile</span></span>
<span data-ttu-id="77b5f-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="77b5f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77b5f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77b5f-123">-ResourceGroupName</span></span>
<span data-ttu-id="77b5f-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="77b5f-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b5f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77b5f-125">-ResourceId</span></span>
<span data-ttu-id="77b5f-126">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="77b5f-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77b5f-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="77b5f-127">-WorkspaceName</span></span>
<span data-ttu-id="77b5f-128">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="77b5f-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b5f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77b5f-129">CommonParameters</span></span>
<span data-ttu-id="77b5f-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77b5f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77b5f-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77b5f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77b5f-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77b5f-132">INPUTS</span></span>

### <span data-ttu-id="77b5f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="77b5f-133">System.String</span></span>
## <span data-ttu-id="77b5f-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77b5f-134">OUTPUTS</span></span>

### <span data-ttu-id="77b5f-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="77b5f-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="77b5f-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="77b5f-136">NOTES</span></span>

## <span data-ttu-id="77b5f-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77b5f-137">RELATED LINKS</span></span>
