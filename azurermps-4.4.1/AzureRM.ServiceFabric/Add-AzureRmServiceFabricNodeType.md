---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 305e406a3f2ef723eb0431b495106bb688ffe61c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549848"
---
# <span data-ttu-id="e8aa3-101">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="e8aa3-101">Add-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="e8aa3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="e8aa3-103">Dodawanie nowego typu węzła do istniejącego klastra.</span><span class="sxs-lookup"><span data-stu-id="e8aa3-103">Add a new node type to the existing cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8aa3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8aa3-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -Capacity <Int32> -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8aa3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e8aa3-105">DESCRIPTION</span></span>
<span data-ttu-id="e8aa3-106">Dodawanie nowego typu węzła do istniejącego klastra.</span><span class="sxs-lookup"><span data-stu-id="e8aa3-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="e8aa3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8aa3-107">EXAMPLES</span></span>

### <span data-ttu-id="e8aa3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e8aa3-108">Example 1</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="e8aa3-109">To polecenie doda nowy NodeType ' N2 ' o pojemności 5, a nazwa administratora maszyny wirtualnej to "AdminName".</span><span class="sxs-lookup"><span data-stu-id="e8aa3-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="e8aa3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8aa3-110">PARAMETERS</span></span>

### <span data-ttu-id="e8aa3-111">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="e8aa3-111">-Capacity</span></span>
<span data-ttu-id="e8aa3-112">Ciąż</span><span class="sxs-lookup"><span data-stu-id="e8aa3-112">Capacity</span></span>

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

### <span data-ttu-id="e8aa3-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e8aa3-113">-Name</span></span>
<span data-ttu-id="e8aa3-114">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="e8aa3-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="e8aa3-115">-NodeType</span><span class="sxs-lookup"><span data-stu-id="e8aa3-115">-NodeType</span></span>
<span data-ttu-id="e8aa3-116">Nazwa typu węzła.</span><span class="sxs-lookup"><span data-stu-id="e8aa3-116">The node type name.</span></span>

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

### <span data-ttu-id="e8aa3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8aa3-117">-ResourceGroupName</span></span>
<span data-ttu-id="e8aa3-118">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e8aa3-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e8aa3-119">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="e8aa3-119">-Tier</span></span>
<span data-ttu-id="e8aa3-120">Warstwa SKU maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e8aa3-120">Vm Sku Tier.</span></span>

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

### <span data-ttu-id="e8aa3-121">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="e8aa3-121">-DurabilityLevel</span></span>
<span data-ttu-id="e8aa3-122">Określ poziom trwałości NodeType.</span><span class="sxs-lookup"><span data-stu-id="e8aa3-122">Specify the durability level of the NodeType.</span></span>

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

### <span data-ttu-id="e8aa3-123">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="e8aa3-123">-VmPassword</span></span>
<span data-ttu-id="e8aa3-124">Hasło logowania do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e8aa3-124">The password of login to the Vm.</span></span>

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

### <span data-ttu-id="e8aa3-125">-VmSku</span><span class="sxs-lookup"><span data-stu-id="e8aa3-125">-VmSku</span></span>
<span data-ttu-id="e8aa3-126">Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="e8aa3-126">The sku name.</span></span>

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

### <span data-ttu-id="e8aa3-127">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="e8aa3-127">-VmUserName</span></span>
<span data-ttu-id="e8aa3-128">Nazwa użytkownika służąca do logowania się do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e8aa3-128">The user name for login to Vm.</span></span>

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

### <span data-ttu-id="e8aa3-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e8aa3-129">-Confirm</span></span>
<span data-ttu-id="e8aa3-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8aa3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8aa3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8aa3-131">-WhatIf</span></span>
<span data-ttu-id="e8aa3-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8aa3-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8aa3-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e8aa3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8aa3-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8aa3-134">-DefaultProfile</span></span>
<span data-ttu-id="e8aa3-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8aa3-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8aa3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8aa3-136">CommonParameters</span></span>
<span data-ttu-id="e8aa3-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8aa3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8aa3-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8aa3-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8aa3-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8aa3-139">INPUTS</span></span>

### <span data-ttu-id="e8aa3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e8aa3-140">System.String</span></span>
<span data-ttu-id="e8aa3-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e8aa3-141">System.Int32</span></span>

## <span data-ttu-id="e8aa3-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8aa3-142">OUTPUTS</span></span>

### <span data-ttu-id="e8aa3-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="e8aa3-143">System.Object</span></span>

## <span data-ttu-id="e8aa3-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8aa3-144">NOTES</span></span>

## <span data-ttu-id="e8aa3-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8aa3-145">RELATED LINKS</span></span>

