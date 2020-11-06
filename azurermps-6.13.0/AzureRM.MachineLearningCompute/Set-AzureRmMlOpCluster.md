---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/set-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
ms.openlocfilehash: cbe72d14eac4864b784f31c4a800db09fc38b042
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545144"
---
# <span data-ttu-id="d46b1-101">Set-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="d46b1-101">Set-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="d46b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d46b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d46b1-103">Ustawia właściwości klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="d46b1-103">Sets the properties of an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d46b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d46b1-104">SYNTAX</span></span>

### <span data-ttu-id="d46b1-105">SetByIndividualParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d46b1-105">SetByIndividualParameters (Default)</span></span>
```
Set-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d46b1-106">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="d46b1-106">SetByInputObject</span></span>
```
Set-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d46b1-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d46b1-107">SetByResourceId</span></span>
```
Set-AzureRmMlOpCluster -ResourceId <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d46b1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d46b1-108">DESCRIPTION</span></span>
<span data-ttu-id="d46b1-109">Ustawia wszystkie właściwości klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="d46b1-109">Sets all the properties of an operationalization cluster.</span></span> <span data-ttu-id="d46b1-110">Ponieważ podczas korzystania z obiektu klastra ustawiane są wszystkie właściwości, należy przekazać w pełni prawidłowy obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="d46b1-110">Since it sets all the properties when using a cluster object a fully valid input object must be passed.</span></span> <span data-ttu-id="d46b1-111">Właściwości tylko do odczytu będą ignorowane.</span><span class="sxs-lookup"><span data-stu-id="d46b1-111">Read-only properties will be ignored.</span></span> <span data-ttu-id="d46b1-112">Obecnie można aktualizować tylko niektóre właściwości, jak pokazano w zestawach parametrów.</span><span class="sxs-lookup"><span data-stu-id="d46b1-112">Only some properties are currently updatable, as shown in the parameter sets.</span></span>

## <span data-ttu-id="d46b1-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d46b1-113">EXAMPLES</span></span>

### <span data-ttu-id="d46b1-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d46b1-114">Example 1</span></span>
<span data-ttu-id="d46b1-115">Aktualizowanie klastra przy użyciu poszczególnych parametrów.</span><span class="sxs-lookup"><span data-stu-id="d46b1-115">Update a cluster using individual parameters.</span></span>

```
PS C:\> Set-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster -AgentCount 5
```

### <span data-ttu-id="d46b1-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d46b1-116">Example 2</span></span>
<span data-ttu-id="d46b1-117">Aktualizowanie klastra przy użyciu obiektu wejściowego.</span><span class="sxs-lookup"><span data-stu-id="d46b1-117">Update a cluster using an input object.</span></span>

```
PS C:\> $cluster = Get-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster
PS C:\> $cluster.ContainerService.AgentCount = 5
PS C:\> Set-AzureRmMlOpCluster -InputObject $cluster
```

## <span data-ttu-id="d46b1-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d46b1-118">PARAMETERS</span></span>

### <span data-ttu-id="d46b1-119">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="d46b1-119">-AgentCount</span></span>
<span data-ttu-id="d46b1-120">Liczba węzłów agenta w klastrze ACS.</span><span class="sxs-lookup"><span data-stu-id="d46b1-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d46b1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d46b1-121">-DefaultProfile</span></span>
<span data-ttu-id="d46b1-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d46b1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d46b1-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d46b1-123">-InputObject</span></span>
<span data-ttu-id="d46b1-124">Właściwości klastra operationalization.</span><span class="sxs-lookup"><span data-stu-id="d46b1-124">The operationalization cluster properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: SetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d46b1-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d46b1-125">-Name</span></span>
<span data-ttu-id="d46b1-126">Nazwa klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="d46b1-126">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46b1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d46b1-127">-ResourceGroupName</span></span>
<span data-ttu-id="d46b1-128">Nazwa grupy zasobów dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="d46b1-128">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46b1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d46b1-129">-ResourceId</span></span>
<span data-ttu-id="d46b1-130">Identyfikator zasobu platformy Azure dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="d46b1-130">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d46b1-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="d46b1-131">-SslCertificate</span></span>
<span data-ttu-id="d46b1-132">Dane certyfikatu SSL w formacie PEM.</span><span class="sxs-lookup"><span data-stu-id="d46b1-132">The SSL certificate data in PEM format.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d46b1-133">-SslCName</span><span class="sxs-lookup"><span data-stu-id="d46b1-133">-SslCName</span></span>
<span data-ttu-id="d46b1-134">Certyfikat CName dla certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="d46b1-134">The CName for the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d46b1-135">-SslKey</span><span class="sxs-lookup"><span data-stu-id="d46b1-135">-SslKey</span></span>
<span data-ttu-id="d46b1-136">Dane klucza SSL w formacie PEM.</span><span class="sxs-lookup"><span data-stu-id="d46b1-136">The SSL key data in PEM format.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d46b1-137">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="d46b1-137">-SslStatus</span></span>
<span data-ttu-id="d46b1-138">Stan protokołu SSL.</span><span class="sxs-lookup"><span data-stu-id="d46b1-138">SSL status.</span></span>
<span data-ttu-id="d46b1-139">Możliwe wartości to "włączone" i "wyłączone".</span><span class="sxs-lookup"><span data-stu-id="d46b1-139">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d46b1-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d46b1-140">-Confirm</span></span>
<span data-ttu-id="d46b1-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d46b1-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d46b1-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d46b1-142">-WhatIf</span></span>
<span data-ttu-id="d46b1-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d46b1-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d46b1-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d46b1-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d46b1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d46b1-145">CommonParameters</span></span>
<span data-ttu-id="d46b1-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d46b1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d46b1-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d46b1-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d46b1-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d46b1-148">INPUTS</span></span>

### <span data-ttu-id="d46b1-149">Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="d46b1-149">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="d46b1-150">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d46b1-150">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="d46b1-151">System. String</span><span class="sxs-lookup"><span data-stu-id="d46b1-151">System.String</span></span>

### <span data-ttu-id="d46b1-152">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d46b1-152">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d46b1-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d46b1-153">OUTPUTS</span></span>

### <span data-ttu-id="d46b1-154">Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="d46b1-154">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="d46b1-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d46b1-155">NOTES</span></span>

## <span data-ttu-id="d46b1-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d46b1-156">RELATED LINKS</span></span>
