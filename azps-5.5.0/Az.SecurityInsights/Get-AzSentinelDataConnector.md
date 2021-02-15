---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
ms.openlocfilehash: e2505d53b0443bd048fb5d15df225adb0cba0980
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189130"
---
# <span data-ttu-id="a943e-101">Get-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="a943e-101">Get-AzSentinelDataConnector</span></span>

## <span data-ttu-id="a943e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a943e-102">SYNOPSIS</span></span>
<span data-ttu-id="a943e-103">Uzyskiwanie łącznika danych.</span><span class="sxs-lookup"><span data-stu-id="a943e-103">Get a Data Connector.</span></span>

## <span data-ttu-id="a943e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a943e-104">SYNTAX</span></span>

### <span data-ttu-id="a943e-105">WorkspaceScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a943e-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a943e-106">DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="a943e-106">DataConnectorId</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a943e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a943e-107">ResourceId</span></span>
```
Get-AzSentinelDataConnector -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a943e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a943e-108">DESCRIPTION</span></span>
<span data-ttu-id="a943e-109">Polecenie **cmdlet Get-AzSentinelDataConnector** pobiera łącznik danych z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a943e-109">The **Get-AzSentinelDataConnector** cmdlet gets a Data Connector from the specified workspace.</span></span>
<span data-ttu-id="a943e-110">W przypadku określenia *parametru DataConnectorId* zwracany jest jeden obiekt **DataConnector.**</span><span class="sxs-lookup"><span data-stu-id="a943e-110">If you specify the *DataConnectorId* parameter, a single **DataConnector** object is returned.</span></span>
<span data-ttu-id="a943e-111">Jeśli parametr *DataConnectorId nie zostanie* określony, zostanie zwrócona tablica zawierająca wszystkie łączniki danych w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="a943e-111">If you do not specify the *DataConnectorId* parameter, an array containing all of the Data Connectors in the specified workspace are returned.</span></span>
<span data-ttu-id="a943e-112">Za pomocą obiektu **DataConnector** można na przykład wyłączyć łącznik **danych.**</span><span class="sxs-lookup"><span data-stu-id="a943e-112">You can use the **DataConnector** object to update the Data Connector, for example you can disable the **DataConnector**.</span></span>

## <span data-ttu-id="a943e-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a943e-113">EXAMPLES</span></span>

### <span data-ttu-id="a943e-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a943e-114">Example 1</span></span>
```powershell
PS C:\> $DataConnectors = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="a943e-115">W tym przykładzie wszystkie połączenia **danych są** przechowywane w określonym obszarze roboczym, a następnie przechowywane w $DataConnectors danych.</span><span class="sxs-lookup"><span data-stu-id="a943e-115">This example gets all of the **DataConnectors** in the specified workspace, and then stores it in the $DataConnectors variable.</span></span>

### <span data-ttu-id="a943e-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a943e-116">Example 2</span></span>
```powershell
PS C:\> $DataConnector = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="a943e-117">Ten przykład pobiera **program DataConnector** w określonym obszarze roboczym, a następnie zapisuje go w $DataConnector danych.</span><span class="sxs-lookup"><span data-stu-id="a943e-117">This example gets an **DataConnector** in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="a943e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a943e-118">PARAMETERS</span></span>

### <span data-ttu-id="a943e-119">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="a943e-119">-DataConnectorId</span></span>
<span data-ttu-id="a943e-120">Identyfikator łącznika danych.</span><span class="sxs-lookup"><span data-stu-id="a943e-120">Data Connector Id.</span></span>

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

### <span data-ttu-id="a943e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a943e-121">-DefaultProfile</span></span>
<span data-ttu-id="a943e-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a943e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a943e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a943e-123">-ResourceGroupName</span></span>
<span data-ttu-id="a943e-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a943e-124">Resource group name.</span></span>

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

### <span data-ttu-id="a943e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a943e-125">-ResourceId</span></span>
<span data-ttu-id="a943e-126">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="a943e-126">Resource Id.</span></span>

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

### <span data-ttu-id="a943e-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a943e-127">-WorkspaceName</span></span>
<span data-ttu-id="a943e-128">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a943e-128">Workspace Name.</span></span>

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

### <span data-ttu-id="a943e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a943e-129">CommonParameters</span></span>
<span data-ttu-id="a943e-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a943e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a943e-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a943e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a943e-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a943e-132">INPUTS</span></span>

### <span data-ttu-id="a943e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a943e-133">System.String</span></span>
## <span data-ttu-id="a943e-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a943e-134">OUTPUTS</span></span>

### <span data-ttu-id="a943e-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="a943e-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="a943e-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a943e-136">NOTES</span></span>

## <span data-ttu-id="a943e-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a943e-137">RELATED LINKS</span></span>
