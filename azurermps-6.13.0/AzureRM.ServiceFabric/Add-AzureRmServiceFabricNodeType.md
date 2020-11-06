---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 573dd2f4681ae140fbe98de5d9a7e9df4e2dc764
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543404"
---
# <span data-ttu-id="ad37a-101">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="ad37a-101">Add-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="ad37a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad37a-102">SYNOPSIS</span></span>
<span data-ttu-id="ad37a-103">Dodawanie nowego typu węzła do istniejącego klastra.</span><span class="sxs-lookup"><span data-stu-id="ad37a-103">Add a new node type to the existing cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad37a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad37a-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad37a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ad37a-105">DESCRIPTION</span></span>
<span data-ttu-id="ad37a-106">Dodawanie nowego typu węzła do istniejącego klastra.</span><span class="sxs-lookup"><span data-stu-id="ad37a-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="ad37a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad37a-107">EXAMPLES</span></span>

### <span data-ttu-id="ad37a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ad37a-108">Example 1</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="ad37a-109">To polecenie doda nowy NodeType ' N2 ' o pojemności 5, a nazwa administratora maszyny wirtualnej to "AdminName".</span><span class="sxs-lookup"><span data-stu-id="ad37a-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="ad37a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad37a-110">PARAMETERS</span></span>

### <span data-ttu-id="ad37a-111">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="ad37a-111">-Capacity</span></span>
<span data-ttu-id="ad37a-112">Ciąż</span><span class="sxs-lookup"><span data-stu-id="ad37a-112">Capacity</span></span>

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

### <span data-ttu-id="ad37a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad37a-113">-DefaultProfile</span></span>
<span data-ttu-id="ad37a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad37a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad37a-115">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="ad37a-115">-DurabilityLevel</span></span>
<span data-ttu-id="ad37a-116">Określ poziom trwałości NodeType.</span><span class="sxs-lookup"><span data-stu-id="ad37a-116">Specify the durability level of the NodeType.</span></span>

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

### <span data-ttu-id="ad37a-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ad37a-117">-Name</span></span>
<span data-ttu-id="ad37a-118">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="ad37a-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ad37a-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="ad37a-119">-NodeType</span></span>
<span data-ttu-id="ad37a-120">Nazwa typu węzła.</span><span class="sxs-lookup"><span data-stu-id="ad37a-120">The node type name.</span></span>

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

### <span data-ttu-id="ad37a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad37a-121">-ResourceGroupName</span></span>
<span data-ttu-id="ad37a-122">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ad37a-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ad37a-123">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="ad37a-123">-Tier</span></span>
<span data-ttu-id="ad37a-124">Warstwa SKU maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ad37a-124">Vm Sku Tier.</span></span>

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

### <span data-ttu-id="ad37a-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="ad37a-125">-VmPassword</span></span>
<span data-ttu-id="ad37a-126">Hasło logowania do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ad37a-126">The password of login to the Vm.</span></span>

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

### <span data-ttu-id="ad37a-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="ad37a-127">-VmSku</span></span>
<span data-ttu-id="ad37a-128">Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="ad37a-128">The sku name.</span></span>

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

### <span data-ttu-id="ad37a-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="ad37a-129">-VmUserName</span></span>
<span data-ttu-id="ad37a-130">Nazwa użytkownika służąca do logowania się do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ad37a-130">The user name for login to Vm.</span></span>

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

### <span data-ttu-id="ad37a-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad37a-131">-Confirm</span></span>
<span data-ttu-id="ad37a-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad37a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad37a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad37a-133">-WhatIf</span></span>
<span data-ttu-id="ad37a-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad37a-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad37a-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ad37a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad37a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad37a-136">CommonParameters</span></span>
<span data-ttu-id="ad37a-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad37a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad37a-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad37a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad37a-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad37a-139">INPUTS</span></span>

### <span data-ttu-id="ad37a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ad37a-140">System.String</span></span>
<span data-ttu-id="ad37a-141">Parametry: NodeType (ByValue), warstwa (ByValue), VmSku (ByValue), VmUserName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ad37a-141">Parameters: NodeType (ByValue), Tier (ByValue), VmSku (ByValue), VmUserName (ByValue)</span></span>

### <span data-ttu-id="ad37a-142">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ad37a-142">System.Int32</span></span>
<span data-ttu-id="ad37a-143">Parametry: wydajność (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ad37a-143">Parameters: Capacity (ByValue)</span></span>

### <span data-ttu-id="ad37a-144">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="ad37a-144">System.Security.SecureString</span></span>
<span data-ttu-id="ad37a-145">Parametry: VmPassword (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ad37a-145">Parameters: VmPassword (ByValue)</span></span>

### <span data-ttu-id="ad37a-146">Microsoft. Azure. Commands. servicefabric. MODELES. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="ad37a-146">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="ad37a-147">Parametry: DurabilityLevel (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ad37a-147">Parameters: DurabilityLevel (ByValue)</span></span>

## <span data-ttu-id="ad37a-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad37a-148">OUTPUTS</span></span>

### <span data-ttu-id="ad37a-149">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="ad37a-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="ad37a-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad37a-150">NOTES</span></span>

## <span data-ttu-id="ad37a-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad37a-151">RELATED LINKS</span></span>
