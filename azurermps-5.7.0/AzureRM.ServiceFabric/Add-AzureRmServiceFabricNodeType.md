---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 0bae150e60332e4f1bb0ee4f2ee67699c13eb5e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526593"
---
# <span data-ttu-id="b89e7-101">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="b89e7-101">Add-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="b89e7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b89e7-102">SYNOPSIS</span></span>
<span data-ttu-id="b89e7-103">Dodawanie nowego typu węzła do istniejącego klastra.</span><span class="sxs-lookup"><span data-stu-id="b89e7-103">Add a new node type to the existing cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b89e7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b89e7-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b89e7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b89e7-105">DESCRIPTION</span></span>
<span data-ttu-id="b89e7-106">Dodawanie nowego typu węzła do istniejącego klastra.</span><span class="sxs-lookup"><span data-stu-id="b89e7-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="b89e7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b89e7-107">EXAMPLES</span></span>

### <span data-ttu-id="b89e7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b89e7-108">Example 1</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="b89e7-109">To polecenie doda nowy NodeType ' N2 ' o pojemności 5, a nazwa administratora maszyny wirtualnej to "AdminName".</span><span class="sxs-lookup"><span data-stu-id="b89e7-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="b89e7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b89e7-110">PARAMETERS</span></span>

### <span data-ttu-id="b89e7-111">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="b89e7-111">-Capacity</span></span>
<span data-ttu-id="b89e7-112">Ciąż</span><span class="sxs-lookup"><span data-stu-id="b89e7-112">Capacity</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b89e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b89e7-113">-DefaultProfile</span></span>
<span data-ttu-id="b89e7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b89e7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b89e7-115">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="b89e7-115">-DurabilityLevel</span></span>
<span data-ttu-id="b89e7-116">Określ poziom trwałości NodeType.</span><span class="sxs-lookup"><span data-stu-id="b89e7-116">Specify the durability level of the NodeType.</span></span>

```yaml
Type: DurabilityLevel
Parameter Sets: (All)
Aliases: 
Accepted values: Bronze, Silver, Gold

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b89e7-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b89e7-117">-Name</span></span>
<span data-ttu-id="b89e7-118">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="b89e7-118">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b89e7-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="b89e7-119">-NodeType</span></span>
<span data-ttu-id="b89e7-120">Nazwa typu węzła.</span><span class="sxs-lookup"><span data-stu-id="b89e7-120">The node type name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b89e7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b89e7-121">-ResourceGroupName</span></span>
<span data-ttu-id="b89e7-122">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b89e7-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b89e7-123">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="b89e7-123">-Tier</span></span>
<span data-ttu-id="b89e7-124">Warstwa SKU maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b89e7-124">Vm Sku Tier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b89e7-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="b89e7-125">-VmPassword</span></span>
<span data-ttu-id="b89e7-126">Hasło logowania do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b89e7-126">The password of login to the Vm.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b89e7-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="b89e7-127">-VmSku</span></span>
<span data-ttu-id="b89e7-128">Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="b89e7-128">The sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b89e7-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="b89e7-129">-VmUserName</span></span>
<span data-ttu-id="b89e7-130">Nazwa użytkownika służąca do logowania się do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b89e7-130">The user name for login to Vm.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b89e7-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b89e7-131">-Confirm</span></span>
<span data-ttu-id="b89e7-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b89e7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b89e7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b89e7-133">-WhatIf</span></span>
<span data-ttu-id="b89e7-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b89e7-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b89e7-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b89e7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b89e7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b89e7-136">CommonParameters</span></span>
<span data-ttu-id="b89e7-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b89e7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b89e7-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b89e7-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b89e7-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b89e7-139">INPUTS</span></span>

### <span data-ttu-id="b89e7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b89e7-140">System.String</span></span>
<span data-ttu-id="b89e7-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b89e7-141">System.Int32</span></span>

## <span data-ttu-id="b89e7-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b89e7-142">OUTPUTS</span></span>

### <span data-ttu-id="b89e7-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="b89e7-143">System.Object</span></span>

## <span data-ttu-id="b89e7-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b89e7-144">NOTES</span></span>

## <span data-ttu-id="b89e7-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b89e7-145">RELATED LINKS</span></span>

