---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5141D84C-3C58-42B9-890F-C3C9049BC1C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
ms.openlocfilehash: b3421fa4382912d11a3e3a28b81acffb7be123a2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304086"
---
# <span data-ttu-id="dda22-101">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="dda22-101">Set-AzHDInsightClusterDiskEncryptionKey</span></span>

## <span data-ttu-id="dda22-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dda22-102">SYNOPSIS</span></span>
<span data-ttu-id="dda22-103">Obraca klucz szyfrowania dysku określonego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="dda22-103">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

## <span data-ttu-id="dda22-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dda22-104">SYNTAX</span></span>

### <span data-ttu-id="dda22-105">SetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dda22-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceGroupName] <String> [-Name] <String>
 -EncryptionKeyName <String> -EncryptionKeyVersion <String> -EncryptionVaultUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dda22-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dda22-106">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceId] <String> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dda22-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dda22-107">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-InputObject] <AzureHDInsightCluster> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dda22-108">Opis</span><span class="sxs-lookup"><span data-stu-id="dda22-108">DESCRIPTION</span></span>
<span data-ttu-id="dda22-109">Obróć klucz szyfrowania dysku określonego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="dda22-109">Rotate the disk encryption key of the specified HDInsight cluster.</span></span> <span data-ttu-id="dda22-110">W przypadku tej operacji klaster musi mieć dostęp zarówno do bieżącego klucza, jak i do zamierzonego nowego klucza, w przeciwnym razie operacja obracania klucza zakończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="dda22-110">For this operation, the cluster must have access to both the current key and the intended new key, otherwise the rotate key operation will fail.</span></span>

## <span data-ttu-id="dda22-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dda22-111">EXAMPLES</span></span>

### <span data-ttu-id="dda22-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dda22-112">Example 1</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterResourceGroupName = "Group"
        $clusterName = "your-cmk-cluster"

Set-AzHDInsightClusterDiskEncryptionKey `
        -ResourceGroupName $clusterResourceGroupName `
        -ClusterName $clusterName `
        -EncryptionKeyName new-key `
        -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
        -EncryptionKeyVersion 00000000000000000000000000000000
```

### <span data-ttu-id="dda22-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="dda22-113">Example 2</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterName = "your-cmk-cluster"

$cluster= Get-AzHDInsightCluster -ClusterName $clusterName 
$cluster |  Set-AzHDInsightClusterDiskEncryptionKey `
    -EncryptionKeyName new-key `
    -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
    -EncryptionKeyVersion 00000000000000000000000000000000
```

## <span data-ttu-id="dda22-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dda22-114">PARAMETERS</span></span>

### <span data-ttu-id="dda22-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dda22-115">-DefaultProfile</span></span>
<span data-ttu-id="dda22-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dda22-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dda22-117">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="dda22-117">-EncryptionKeyName</span></span>
<span data-ttu-id="dda22-118">Pobiera lub ustawia nazwę klucza szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="dda22-118">Gets or sets the encryption key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda22-119">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="dda22-119">-EncryptionKeyVersion</span></span>
<span data-ttu-id="dda22-120">Pobiera lub ustawia wersję klucza szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="dda22-120">Gets or sets the encryption key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda22-121">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="dda22-121">-EncryptionVaultUri</span></span>
<span data-ttu-id="dda22-122">Pobiera lub ustawia identyfikator URI magazynu szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="dda22-122">Gets or sets the encryption vault uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda22-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dda22-123">-InputObject</span></span>
<span data-ttu-id="dda22-124">Pobiera lub ustawia obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="dda22-124">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dda22-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dda22-125">-Name</span></span>
<span data-ttu-id="dda22-126">Pobiera lub ustawia nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="dda22-126">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda22-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dda22-127">-ResourceGroupName</span></span>
<span data-ttu-id="dda22-128">Pobiera lub ustawia nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dda22-128">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda22-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dda22-129">-ResourceId</span></span>
<span data-ttu-id="dda22-130">Pobiera lub ustawia identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="dda22-130">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda22-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dda22-131">-Confirm</span></span>
<span data-ttu-id="dda22-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dda22-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dda22-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dda22-133">-WhatIf</span></span>
<span data-ttu-id="dda22-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dda22-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dda22-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dda22-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dda22-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dda22-136">CommonParameters</span></span>
<span data-ttu-id="dda22-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dda22-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dda22-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dda22-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dda22-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dda22-139">INPUTS</span></span>

### <span data-ttu-id="dda22-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="dda22-140">None</span></span>

## <span data-ttu-id="dda22-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dda22-141">OUTPUTS</span></span>

### <span data-ttu-id="dda22-142">Microsoft. Azure. Management. HDInsight. modele. Cluster</span><span class="sxs-lookup"><span data-stu-id="dda22-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="dda22-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dda22-143">NOTES</span></span>

## <span data-ttu-id="dda22-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dda22-144">RELATED LINKS</span></span>

[<span data-ttu-id="dda22-145">Szyfrowanie dysków klucza zarządzanego przez klienta</span><span class="sxs-lookup"><span data-stu-id="dda22-145">Customer-managed key disk encryption</span></span>](https://docs.microsoft.com/en-us/azure/hdinsight/disk-encryption)
