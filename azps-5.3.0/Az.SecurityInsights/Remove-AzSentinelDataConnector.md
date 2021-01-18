---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
ms.openlocfilehash: 19e9dd843cd428a65b371ae933d00c58233de35b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502957"
---
# <span data-ttu-id="670bd-101">Remove-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="670bd-101">Remove-AzSentinelDataConnector</span></span>

## <span data-ttu-id="670bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="670bd-102">SYNOPSIS</span></span>
<span data-ttu-id="670bd-103">Usuwanie łącznika danych.</span><span class="sxs-lookup"><span data-stu-id="670bd-103">Remove a Data Connector.</span></span>

## <span data-ttu-id="670bd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="670bd-104">SYNTAX</span></span>

### <span data-ttu-id="670bd-105">DataConnectorId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="670bd-105">DataConnectorId (Default)</span></span>
```
Remove-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="670bd-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="670bd-106">InputObject</span></span>
```
Remove-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="670bd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="670bd-107">DESCRIPTION</span></span>
<span data-ttu-id="670bd-108">Polecenie cmdlet **Remove-AzSentinelDataConnector** powoduje trwałe usunięcie łącznika danych z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="670bd-108">The **Remove-AzSentinelDataConnector** cmdlet permanently deletes a Data Connector from a specified workspace.</span></span>
<span data-ttu-id="670bd-109">Obiekt programu **dataconnect** można przekazać za pomocą operatora potoku lub można też określić parametry wymagane.</span><span class="sxs-lookup"><span data-stu-id="670bd-109">You can pass an **DataConnector** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="670bd-110">Za pomocą zmiennej Confirm i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="670bd-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="670bd-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="670bd-111">EXAMPLES</span></span>

### <span data-ttu-id="670bd-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="670bd-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="670bd-113">To polecenie powoduje usunięcie programu dataconnect z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="670bd-113">This command removes the DataConnector from the workspace.</span></span>

## <span data-ttu-id="670bd-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="670bd-114">PARAMETERS</span></span>

### <span data-ttu-id="670bd-115">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="670bd-115">-DataConnectorId</span></span>
<span data-ttu-id="670bd-116">Identyfikator łącznika danych.</span><span class="sxs-lookup"><span data-stu-id="670bd-116">Data Connector Id.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="670bd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="670bd-117">-DefaultProfile</span></span>
<span data-ttu-id="670bd-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="670bd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="670bd-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="670bd-119">-InputObject</span></span>
<span data-ttu-id="670bd-120">Inputobject.</span><span class="sxs-lookup"><span data-stu-id="670bd-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="670bd-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="670bd-121">-PassThru</span></span>
<span data-ttu-id="670bd-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="670bd-122">PassThru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="670bd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="670bd-123">-ResourceGroupName</span></span>
<span data-ttu-id="670bd-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="670bd-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="670bd-125">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="670bd-125">-WorkspaceName</span></span>
<span data-ttu-id="670bd-126">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="670bd-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="670bd-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="670bd-127">-Confirm</span></span>
<span data-ttu-id="670bd-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="670bd-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="670bd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="670bd-129">-WhatIf</span></span>
<span data-ttu-id="670bd-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="670bd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="670bd-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="670bd-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="670bd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="670bd-132">CommonParameters</span></span>
<span data-ttu-id="670bd-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="670bd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="670bd-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="670bd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="670bd-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="670bd-135">INPUTS</span></span>

### <span data-ttu-id="670bd-136">System. String</span><span class="sxs-lookup"><span data-stu-id="670bd-136">System.String</span></span>
### <span data-ttu-id="670bd-137">Microsoft. Azure. Commands. SecurityInsights. models. dataconnects. PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="670bd-137">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="670bd-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="670bd-138">OUTPUTS</span></span>

### <span data-ttu-id="670bd-139">Microsoft. Azure. Commands. SecurityInsights. models. dataconnects. PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="670bd-139">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="670bd-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="670bd-140">NOTES</span></span>

## <span data-ttu-id="670bd-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="670bd-141">RELATED LINKS</span></span>
