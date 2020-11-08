---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 3535cc8956643351a6637134cc7dcdd805ed80c3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232548"
---
# <span data-ttu-id="53100-101">Set-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="53100-101">Set-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="53100-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="53100-102">SYNOPSIS</span></span>
<span data-ttu-id="53100-103">Usługa Link Service dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="53100-103">link service for workspace</span></span>

## <span data-ttu-id="53100-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="53100-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-Tags <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-WriteAccessResourceId <String>] [-ResourceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53100-105">Opis</span><span class="sxs-lookup"><span data-stu-id="53100-105">DESCRIPTION</span></span>
<span data-ttu-id="53100-106">Usługa Link Service dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="53100-106">link service for workspace</span></span>

## <span data-ttu-id="53100-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="53100-107">EXAMPLES</span></span>

### <span data-ttu-id="53100-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="53100-108">Example 1</span></span>
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

<span data-ttu-id="53100-109">Łączenie klastra dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="53100-109">link cluster for workspace</span></span>

## <span data-ttu-id="53100-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53100-110">PARAMETERS</span></span>

### <span data-ttu-id="53100-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53100-111">-AsJob</span></span>
<span data-ttu-id="53100-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="53100-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53100-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53100-113">-DefaultProfile</span></span>
<span data-ttu-id="53100-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="53100-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53100-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="53100-115">-LinkedServiceName</span></span>
<span data-ttu-id="53100-116">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="53100-116">The Workspace name.</span></span>

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

### <span data-ttu-id="53100-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53100-117">-ResourceGroupName</span></span>
<span data-ttu-id="53100-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="53100-118">The resource group name.</span></span>

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

### <span data-ttu-id="53100-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53100-119">-ResourceId</span></span>
<span data-ttu-id="53100-120">Identyfikator zasobu zasobu, który zostanie połączony z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="53100-120">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="53100-121">Należy go użyć do łączenia zasobów wymagających dostępu do odczytu.</span><span class="sxs-lookup"><span data-stu-id="53100-121">This should be used for linking resources which require read access</span></span>

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

### <span data-ttu-id="53100-122">-Tagi</span><span class="sxs-lookup"><span data-stu-id="53100-122">-Tags</span></span>
<span data-ttu-id="53100-123">Kolczyk.</span><span class="sxs-lookup"><span data-stu-id="53100-123">Tags.</span></span>

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

### <span data-ttu-id="53100-124">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="53100-124">-WorkspaceName</span></span>
<span data-ttu-id="53100-125">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="53100-125">The Workspace name.</span></span>

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

### <span data-ttu-id="53100-126">-WriteAccessResourceId</span><span class="sxs-lookup"><span data-stu-id="53100-126">-WriteAccessResourceId</span></span>
<span data-ttu-id="53100-127">Identyfikator zasobu zasobu, który zostanie połączony z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="53100-127">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="53100-128">Należy go użyć do łączenia zasobów wymagających uprawnień do zapisu.</span><span class="sxs-lookup"><span data-stu-id="53100-128">This should be used for linking resources which require write access.</span></span>
<span data-ttu-id="53100-129">Klaster musi mieć stan inicjowania obsługi "zakończony powodzeniem" i prawidłowe właściwości magazynu.</span><span class="sxs-lookup"><span data-stu-id="53100-129">Cluster must have provisioning state "Succeeded" and valid keyvault properties.</span></span>

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

### <span data-ttu-id="53100-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="53100-130">-Confirm</span></span>
<span data-ttu-id="53100-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53100-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53100-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53100-132">-WhatIf</span></span>
<span data-ttu-id="53100-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53100-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53100-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="53100-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53100-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53100-135">CommonParameters</span></span>
<span data-ttu-id="53100-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53100-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53100-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53100-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53100-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53100-138">INPUTS</span></span>

### <span data-ttu-id="53100-139">System. String</span><span class="sxs-lookup"><span data-stu-id="53100-139">System.String</span></span>

## <span data-ttu-id="53100-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="53100-140">OUTPUTS</span></span>

### <span data-ttu-id="53100-141">Microsoft. Azure. Commands. OperationalInsights. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="53100-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="53100-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="53100-142">NOTES</span></span>

## <span data-ttu-id="53100-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53100-143">RELATED LINKS</span></span>
