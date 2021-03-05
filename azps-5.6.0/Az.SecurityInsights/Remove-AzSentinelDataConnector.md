---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/remove-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
ms.openlocfilehash: d9dc64124dd4840227b692e2ef21842a19b4adeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978129"
---
# <span data-ttu-id="0c1c2-101">Remove-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="0c1c2-101">Remove-AzSentinelDataConnector</span></span>

## <span data-ttu-id="0c1c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c1c2-102">SYNOPSIS</span></span>
<span data-ttu-id="0c1c2-103">Usuwanie łącznika danych.</span><span class="sxs-lookup"><span data-stu-id="0c1c2-103">Remove a Data Connector.</span></span>

## <span data-ttu-id="0c1c2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0c1c2-104">SYNTAX</span></span>

### <span data-ttu-id="0c1c2-105">DataConnectorId (domyślna)</span><span class="sxs-lookup"><span data-stu-id="0c1c2-105">DataConnectorId (Default)</span></span>
```
Remove-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c1c2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0c1c2-106">InputObject</span></span>
```
Remove-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c1c2-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0c1c2-107">DESCRIPTION</span></span>
<span data-ttu-id="0c1c2-108">Polecenie **cmdlet Remove-AzSentinelDataConnector** trwale usuwa łącznik danych z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="0c1c2-108">The **Remove-AzSentinelDataConnector** cmdlet permanently deletes a Data Connector from a specified workspace.</span></span>
<span data-ttu-id="0c1c2-109">Obiekt **DataConnector** można przekazać za pomocą operatora potoku lub ewentualnie określić wymagane parametry.</span><span class="sxs-lookup"><span data-stu-id="0c1c2-109">You can pass an **DataConnector** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="0c1c2-110">Możesz użyć parametru Confirm i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0c1c2-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="0c1c2-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0c1c2-111">EXAMPLES</span></span>

### <span data-ttu-id="0c1c2-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0c1c2-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="0c1c2-113">To polecenie usuwa program DataConnector z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="0c1c2-113">This command removes the DataConnector from the workspace.</span></span>

## <span data-ttu-id="0c1c2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c1c2-114">PARAMETERS</span></span>

### <span data-ttu-id="0c1c2-115">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="0c1c2-115">-DataConnectorId</span></span>
<span data-ttu-id="0c1c2-116">Identyfikator łącznika danych.</span><span class="sxs-lookup"><span data-stu-id="0c1c2-116">Data Connector Id.</span></span>

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

### <span data-ttu-id="0c1c2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c1c2-117">-DefaultProfile</span></span>
<span data-ttu-id="0c1c2-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c1c2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c1c2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c1c2-119">-InputObject</span></span>
<span data-ttu-id="0c1c2-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="0c1c2-120">InputObject.</span></span>

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

### <span data-ttu-id="0c1c2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c1c2-121">-PassThru</span></span>
<span data-ttu-id="0c1c2-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="0c1c2-122">PassThru</span></span>

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

### <span data-ttu-id="0c1c2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c1c2-123">-ResourceGroupName</span></span>
<span data-ttu-id="0c1c2-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0c1c2-124">Resource group name.</span></span>

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

### <span data-ttu-id="0c1c2-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0c1c2-125">-WorkspaceName</span></span>
<span data-ttu-id="0c1c2-126">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="0c1c2-126">Workspace Name.</span></span>

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

### <span data-ttu-id="0c1c2-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0c1c2-127">-Confirm</span></span>
<span data-ttu-id="0c1c2-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0c1c2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c1c2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c1c2-129">-WhatIf</span></span>
<span data-ttu-id="0c1c2-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c1c2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c1c2-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0c1c2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c1c2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c1c2-132">CommonParameters</span></span>
<span data-ttu-id="0c1c2-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c1c2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c1c2-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c1c2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c1c2-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c1c2-135">INPUTS</span></span>

### <span data-ttu-id="0c1c2-136">System.String</span><span class="sxs-lookup"><span data-stu-id="0c1c2-136">System.String</span></span>
### <span data-ttu-id="0c1c2-137">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="0c1c2-137">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="0c1c2-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c1c2-138">OUTPUTS</span></span>

### <span data-ttu-id="0c1c2-139">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="0c1c2-139">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="0c1c2-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0c1c2-140">NOTES</span></span>

## <span data-ttu-id="0c1c2-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c1c2-141">RELATED LINKS</span></span>
