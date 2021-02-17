---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
ms.openlocfilehash: de512f636b0a326029981e199b13926a9fc5824a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242147"
---
# <span data-ttu-id="a194b-101">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="a194b-101">Add-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="a194b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a194b-102">SYNOPSIS</span></span>
<span data-ttu-id="a194b-103">Dodaj nowy typ węzła do istniejącego klastra.</span><span class="sxs-lookup"><span data-stu-id="a194b-103">Add a new node type to the existing cluster.</span></span>

## <span data-ttu-id="a194b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a194b-104">SYNTAX</span></span>

```
Add-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a194b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a194b-105">DESCRIPTION</span></span>
<span data-ttu-id="a194b-106">Dodaj nowy typ węzła do istniejącego klastra.</span><span class="sxs-lookup"><span data-stu-id="a194b-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="a194b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a194b-107">EXAMPLES</span></span>

### <span data-ttu-id="a194b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a194b-108">Example 1</span></span>
```powershell
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="a194b-109">To polecenie spowoduje dodanie nowego typu NodeType 'n2' o pojemności 5, a nazwa administratora maszyny wirtualnej to "nazwa_administratora".</span><span class="sxs-lookup"><span data-stu-id="a194b-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="a194b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a194b-110">PARAMETERS</span></span>

### <span data-ttu-id="a194b-111">— Pojemność</span><span class="sxs-lookup"><span data-stu-id="a194b-111">-Capacity</span></span>
<span data-ttu-id="a194b-112">Wydajność</span><span class="sxs-lookup"><span data-stu-id="a194b-112">Capacity</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a194b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a194b-113">-DefaultProfile</span></span>
<span data-ttu-id="a194b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a194b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a194b-115">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="a194b-115">-DurabilityLevel</span></span>
<span data-ttu-id="a194b-116">Określ poziom niezawodności typu NodeType.</span><span class="sxs-lookup"><span data-stu-id="a194b-116">Specify the durability level of the NodeType.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel
Parameter Sets: (All)
Aliases:
Accepted values: Bronze, Silver, Gold

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a194b-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a194b-117">-Name</span></span>
<span data-ttu-id="a194b-118">Określanie nazwy klastra</span><span class="sxs-lookup"><span data-stu-id="a194b-118">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a194b-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="a194b-119">-NodeType</span></span>
<span data-ttu-id="a194b-120">Nazwa typu węzła</span><span class="sxs-lookup"><span data-stu-id="a194b-120">The node type name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a194b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a194b-121">-ResourceGroupName</span></span>
<span data-ttu-id="a194b-122">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a194b-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a194b-123">- Warstwa</span><span class="sxs-lookup"><span data-stu-id="a194b-123">-Tier</span></span>
<span data-ttu-id="a194b-124">Warstwa SKU maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a194b-124">Vm Sku Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a194b-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="a194b-125">-VmPassword</span></span>
<span data-ttu-id="a194b-126">Hasło logowania do maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a194b-126">The password for login to the Vm</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a194b-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="a194b-127">-VmSku</span></span>
<span data-ttu-id="a194b-128">Nazwa sKU</span><span class="sxs-lookup"><span data-stu-id="a194b-128">The sku name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a194b-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="a194b-129">-VmUserName</span></span>
<span data-ttu-id="a194b-130">Nazwa użytkownika dla rejestrowania do maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a194b-130">The user name for logging to Vm</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a194b-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a194b-131">-Confirm</span></span>
<span data-ttu-id="a194b-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a194b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a194b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a194b-133">-WhatIf</span></span>
<span data-ttu-id="a194b-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a194b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a194b-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a194b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a194b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a194b-136">CommonParameters</span></span>
<span data-ttu-id="a194b-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a194b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a194b-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a194b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a194b-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a194b-139">INPUTS</span></span>

### <span data-ttu-id="a194b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a194b-140">System.String</span></span>

### <span data-ttu-id="a194b-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a194b-141">System.Int32</span></span>

### <span data-ttu-id="a194b-142">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="a194b-142">System.Security.SecureString</span></span>

### <span data-ttu-id="a194b-143">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="a194b-143">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="a194b-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a194b-144">OUTPUTS</span></span>

### <span data-ttu-id="a194b-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="a194b-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="a194b-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a194b-146">NOTES</span></span>

## <span data-ttu-id="a194b-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a194b-147">RELATED LINKS</span></span>
