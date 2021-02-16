---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 3535cc8956643351a6637134cc7dcdd805ed80c3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186707"
---
# <span data-ttu-id="0a87f-101">Set-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="0a87f-101">Set-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="0a87f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a87f-102">SYNOPSIS</span></span>
<span data-ttu-id="0a87f-103">Usługa łączenia dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="0a87f-103">link service for workspace</span></span>

## <span data-ttu-id="0a87f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0a87f-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-Tags <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-WriteAccessResourceId <String>] [-ResourceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a87f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0a87f-105">DESCRIPTION</span></span>
<span data-ttu-id="0a87f-106">Usługa łączenia dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="0a87f-106">link service for workspace</span></span>

## <span data-ttu-id="0a87f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0a87f-107">EXAMPLES</span></span>

### <span data-ttu-id="0a87f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0a87f-108">Example 1</span></span>
```powershell
Set-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster -WriteAccessResourceId /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}

Id                    : /subscriptions/{subscription}/resourcegroups/{rg-name}/providers/microsoft.operationalinsights/workspaces/{workspace-name}/linkedservices/cluster
Name                  : {cluster-name}/Cluster
Type                  : Microsoft.OperationalInsights/workspaces/linkedServices
ResourceId            :
WriteAccessResourceId : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
ProvisioningState     : ProvisioningAccount
Tags                  :
```

<span data-ttu-id="0a87f-109">Klaster łączy dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="0a87f-109">link cluster for workspace</span></span>

## <span data-ttu-id="0a87f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a87f-110">PARAMETERS</span></span>

### <span data-ttu-id="0a87f-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0a87f-111">-AsJob</span></span>
<span data-ttu-id="0a87f-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0a87f-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a87f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a87f-113">-DefaultProfile</span></span>
<span data-ttu-id="0a87f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0a87f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a87f-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="0a87f-115">-LinkedServiceName</span></span>
<span data-ttu-id="0a87f-116">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="0a87f-116">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a87f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a87f-117">-ResourceGroupName</span></span>
<span data-ttu-id="0a87f-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0a87f-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a87f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a87f-119">-ResourceId</span></span>
<span data-ttu-id="0a87f-120">Identyfikator zasobu, który zostanie połączony z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="0a87f-120">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="0a87f-121">Należy go używać do łączenia zasobów wymagających dostępu do odczytu</span><span class="sxs-lookup"><span data-stu-id="0a87f-121">This should be used for linking resources which require read access</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a87f-122">— Tagi</span><span class="sxs-lookup"><span data-stu-id="0a87f-122">-Tags</span></span>
<span data-ttu-id="0a87f-123">Tagi.</span><span class="sxs-lookup"><span data-stu-id="0a87f-123">Tags.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a87f-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0a87f-124">-WorkspaceName</span></span>
<span data-ttu-id="0a87f-125">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="0a87f-125">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a87f-126">-WriteAccessResourceId</span><span class="sxs-lookup"><span data-stu-id="0a87f-126">-WriteAccessResourceId</span></span>
<span data-ttu-id="0a87f-127">Identyfikator zasobu, który zostanie połączony z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="0a87f-127">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="0a87f-128">Należy go używać do łączenia zasobów wymagających dostępu do zapisu.</span><span class="sxs-lookup"><span data-stu-id="0a87f-128">This should be used for linking resources which require write access.</span></span>
<span data-ttu-id="0a87f-129">Klaster musi mieć stan inicjowania obsługi "Pomyślnie" i prawidłowe właściwości keyvault.</span><span class="sxs-lookup"><span data-stu-id="0a87f-129">Cluster must have provisioning state "Succeeded" and valid keyvault properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a87f-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0a87f-130">-Confirm</span></span>
<span data-ttu-id="0a87f-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0a87f-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a87f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a87f-132">-WhatIf</span></span>
<span data-ttu-id="0a87f-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a87f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a87f-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0a87f-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a87f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a87f-135">CommonParameters</span></span>
<span data-ttu-id="0a87f-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a87f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a87f-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a87f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a87f-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a87f-138">INPUTS</span></span>

### <span data-ttu-id="0a87f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="0a87f-139">System.String</span></span>

## <span data-ttu-id="0a87f-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0a87f-140">OUTPUTS</span></span>

### <span data-ttu-id="0a87f-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="0a87f-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="0a87f-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0a87f-142">NOTES</span></span>

## <span data-ttu-id="0a87f-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a87f-143">RELATED LINKS</span></span>
