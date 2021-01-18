---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
ms.openlocfilehash: e2505d53b0443bd048fb5d15df225adb0cba0980
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502982"
---
# <span data-ttu-id="9fc0b-101">Get-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="9fc0b-101">Get-AzSentinelDataConnector</span></span>

## <span data-ttu-id="9fc0b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9fc0b-102">SYNOPSIS</span></span>
<span data-ttu-id="9fc0b-103">Uzyskaj Łącznik danych.</span><span class="sxs-lookup"><span data-stu-id="9fc0b-103">Get a Data Connector.</span></span>

## <span data-ttu-id="9fc0b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9fc0b-104">SYNTAX</span></span>

### <span data-ttu-id="9fc0b-105">WorkspaceScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9fc0b-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fc0b-106">DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="9fc0b-106">DataConnectorId</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fc0b-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="9fc0b-107">ResourceId</span></span>
```
Get-AzSentinelDataConnector -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9fc0b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9fc0b-108">DESCRIPTION</span></span>
<span data-ttu-id="9fc0b-109">Polecenie cmdlet **Get-AzSentinelDataConnector** pobiera Łącznik danych z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="9fc0b-109">The **Get-AzSentinelDataConnector** cmdlet gets a Data Connector from the specified workspace.</span></span>
<span data-ttu-id="9fc0b-110">Jeśli określisz parametr *DataConnectorId* , zostanie zwrócony pojedynczy obiekt programu **dataconnect** .</span><span class="sxs-lookup"><span data-stu-id="9fc0b-110">If you specify the *DataConnectorId* parameter, a single **DataConnector** object is returned.</span></span>
<span data-ttu-id="9fc0b-111">Jeśli nie określisz parametru *DataConnectorId* , zostanie zwrócona tablica zawierająca wszystkie łączniki danych w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="9fc0b-111">If you do not specify the *DataConnectorId* parameter, an array containing all of the Data Connectors in the specified workspace are returned.</span></span>
<span data-ttu-id="9fc0b-112">Za pomocą obiektu **Dataconnecter** można zaktualizować Łącznik danych, na przykład można wyłączyć program **dataconnect**.</span><span class="sxs-lookup"><span data-stu-id="9fc0b-112">You can use the **DataConnector** object to update the Data Connector, for example you can disable the **DataConnector**.</span></span>

## <span data-ttu-id="9fc0b-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9fc0b-113">EXAMPLES</span></span>

### <span data-ttu-id="9fc0b-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9fc0b-114">Example 1</span></span>
```powershell
PS C:\> $DataConnectors = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="9fc0b-115">W tym przykładzie są pobierane wszystkie **Dataconnectes** w określonym obszarze roboczym, a następnie jest on przechowywany w zmiennej $DataConnectors.</span><span class="sxs-lookup"><span data-stu-id="9fc0b-115">This example gets all of the **DataConnectors** in the specified workspace, and then stores it in the $DataConnectors variable.</span></span>

### <span data-ttu-id="9fc0b-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9fc0b-116">Example 2</span></span>
```powershell
PS C:\> $DataConnector = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="9fc0b-117">W tym przykładzie jest pobierany program **dataconnect** w określonym obszarze roboczym, a następnie przechowywany w zmiennej $DataConnector.</span><span class="sxs-lookup"><span data-stu-id="9fc0b-117">This example gets an **DataConnector** in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="9fc0b-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9fc0b-118">PARAMETERS</span></span>

### <span data-ttu-id="9fc0b-119">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="9fc0b-119">-DataConnectorId</span></span>
<span data-ttu-id="9fc0b-120">Identyfikator łącznika danych.</span><span class="sxs-lookup"><span data-stu-id="9fc0b-120">Data Connector Id.</span></span>

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

### <span data-ttu-id="9fc0b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fc0b-121">-DefaultProfile</span></span>
<span data-ttu-id="9fc0b-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9fc0b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fc0b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fc0b-123">-ResourceGroupName</span></span>
<span data-ttu-id="9fc0b-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9fc0b-124">Resource group name.</span></span>

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

### <span data-ttu-id="9fc0b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fc0b-125">-ResourceId</span></span>
<span data-ttu-id="9fc0b-126">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="9fc0b-126">Resource Id.</span></span>

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

### <span data-ttu-id="9fc0b-127">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="9fc0b-127">-WorkspaceName</span></span>
<span data-ttu-id="9fc0b-128">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="9fc0b-128">Workspace Name.</span></span>

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

### <span data-ttu-id="9fc0b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fc0b-129">CommonParameters</span></span>
<span data-ttu-id="9fc0b-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fc0b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fc0b-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9fc0b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fc0b-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9fc0b-132">INPUTS</span></span>

### <span data-ttu-id="9fc0b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9fc0b-133">System.String</span></span>
## <span data-ttu-id="9fc0b-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9fc0b-134">OUTPUTS</span></span>

### <span data-ttu-id="9fc0b-135">Microsoft. Azure. Commands. SecurityInsights. models. dataconnects. PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="9fc0b-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="9fc0b-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9fc0b-136">NOTES</span></span>

## <span data-ttu-id="9fc0b-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9fc0b-137">RELATED LINKS</span></span>
