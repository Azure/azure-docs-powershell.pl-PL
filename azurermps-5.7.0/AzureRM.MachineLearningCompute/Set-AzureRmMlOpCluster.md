---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/set-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
ms.openlocfilehash: 142dd983b00b578f47e2c1f2eebcbd0686614430
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719171"
---
# <span data-ttu-id="a82ca-101">Set-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="a82ca-101">Set-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="a82ca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a82ca-102">SYNOPSIS</span></span>
<span data-ttu-id="a82ca-103">Ustawia właściwości klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="a82ca-103">Sets the properties of an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a82ca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a82ca-104">SYNTAX</span></span>

### <span data-ttu-id="a82ca-105">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="a82ca-105">SetByInputObject</span></span>
```
Set-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a82ca-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a82ca-106">SetByResourceId</span></span>
```
Set-AzureRmMlOpCluster -ResourceId <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a82ca-107">SetByIndividualParameters</span><span class="sxs-lookup"><span data-stu-id="a82ca-107">SetByIndividualParameters</span></span>
```
Set-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a82ca-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a82ca-108">DESCRIPTION</span></span>
<span data-ttu-id="a82ca-109">Ustawia wszystkie właściwości klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="a82ca-109">Sets all the properties of an operationalization cluster.</span></span> <span data-ttu-id="a82ca-110">Ponieważ podczas korzystania z obiektu klastra ustawiane są wszystkie właściwości, należy przekazać w pełni prawidłowy obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="a82ca-110">Since it sets all the properties when using a cluster object a fully valid input object must be passed.</span></span> <span data-ttu-id="a82ca-111">Właściwości tylko do odczytu będą ignorowane.</span><span class="sxs-lookup"><span data-stu-id="a82ca-111">Read-only properties will be ignored.</span></span> <span data-ttu-id="a82ca-112">Obecnie można aktualizować tylko niektóre właściwości, jak pokazano w zestawach parametrów.</span><span class="sxs-lookup"><span data-stu-id="a82ca-112">Only some properties are currently updatable, as shown in the parameter sets.</span></span>

## <span data-ttu-id="a82ca-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a82ca-113">EXAMPLES</span></span>

### <span data-ttu-id="a82ca-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a82ca-114">Example 1</span></span>
<span data-ttu-id="a82ca-115">Aktualizowanie klastra przy użyciu poszczególnych parametrów.</span><span class="sxs-lookup"><span data-stu-id="a82ca-115">Update a cluster using individual parameters.</span></span>
```
PS C:\> Set-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster -AgentCount 5
```

### <span data-ttu-id="a82ca-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a82ca-116">Example 2</span></span>
<span data-ttu-id="a82ca-117">Aktualizowanie klastra przy użyciu obiektu wejściowego.</span><span class="sxs-lookup"><span data-stu-id="a82ca-117">Update a cluster using an input object.</span></span>
```
PS C:\> $cluster = Get-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster
PS C:\> $cluster.ContainerService.AgentCount = 5
PS C:\> Set-AzureRmMlOpCluster -InputObject $cluster
```

## <span data-ttu-id="a82ca-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a82ca-118">PARAMETERS</span></span>

### <span data-ttu-id="a82ca-119">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="a82ca-119">-AgentCount</span></span>
<span data-ttu-id="a82ca-120">Liczba węzłów agenta w klastrze ACS.</span><span class="sxs-lookup"><span data-stu-id="a82ca-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a82ca-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a82ca-121">-DefaultProfile</span></span>
<span data-ttu-id="a82ca-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a82ca-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a82ca-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a82ca-123">-InputObject</span></span>
<span data-ttu-id="a82ca-124">Właściwości klastra operationalization.</span><span class="sxs-lookup"><span data-stu-id="a82ca-124">The operationalization cluster properties.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: SetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a82ca-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a82ca-125">-Name</span></span>
<span data-ttu-id="a82ca-126">Nazwa klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="a82ca-126">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: SetByIndividualParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a82ca-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a82ca-127">-ResourceGroupName</span></span>
<span data-ttu-id="a82ca-128">Nazwa grupy zasobów dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="a82ca-128">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: SetByIndividualParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a82ca-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a82ca-129">-ResourceId</span></span>
<span data-ttu-id="a82ca-130">Identyfikator zasobu platformy Azure dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="a82ca-130">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a82ca-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="a82ca-131">-SslCertificate</span></span>
<span data-ttu-id="a82ca-132">Dane certyfikatu SSL w formacie PEM.</span><span class="sxs-lookup"><span data-stu-id="a82ca-132">The SSL certificate data in PEM format.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a82ca-133">-SslCName</span><span class="sxs-lookup"><span data-stu-id="a82ca-133">-SslCName</span></span>
<span data-ttu-id="a82ca-134">Certyfikat CName dla certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="a82ca-134">The CName for the SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a82ca-135">-SslKey</span><span class="sxs-lookup"><span data-stu-id="a82ca-135">-SslKey</span></span>
<span data-ttu-id="a82ca-136">Dane klucza SSL w formacie PEM.</span><span class="sxs-lookup"><span data-stu-id="a82ca-136">The SSL key data in PEM format.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a82ca-137">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="a82ca-137">-SslStatus</span></span>
<span data-ttu-id="a82ca-138">Stan protokołu SSL.</span><span class="sxs-lookup"><span data-stu-id="a82ca-138">SSL status.</span></span>
<span data-ttu-id="a82ca-139">Możliwe wartości to "włączone" i "wyłączone".</span><span class="sxs-lookup"><span data-stu-id="a82ca-139">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a82ca-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a82ca-140">-Confirm</span></span>
<span data-ttu-id="a82ca-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a82ca-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a82ca-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a82ca-142">-WhatIf</span></span>
<span data-ttu-id="a82ca-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a82ca-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a82ca-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a82ca-144">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="a82ca-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a82ca-145">INPUTS</span></span>

### <span data-ttu-id="a82ca-146">Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="a82ca-146">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="a82ca-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a82ca-147">System.String</span></span>
### <span data-ttu-id="a82ca-148">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a82ca-148">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>


## <span data-ttu-id="a82ca-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a82ca-149">OUTPUTS</span></span>

### <span data-ttu-id="a82ca-150">Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="a82ca-150">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>


## <span data-ttu-id="a82ca-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a82ca-151">NOTES</span></span>

## <span data-ttu-id="a82ca-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a82ca-152">RELATED LINKS</span></span>

