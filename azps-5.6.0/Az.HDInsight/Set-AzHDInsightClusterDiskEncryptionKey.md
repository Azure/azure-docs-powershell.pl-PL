---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5141D84C-3C58-42B9-890F-C3C9049BC1C5
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightclusterdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
ms.openlocfilehash: addf0e06a3df625bde5b46cc8089fc89ced832dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984635"
---
# <span data-ttu-id="6fd56-101">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6fd56-101">Set-AzHDInsightClusterDiskEncryptionKey</span></span>

## <span data-ttu-id="6fd56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fd56-102">SYNOPSIS</span></span>
<span data-ttu-id="6fd56-103">Obraca klucz szyfrowania dysku określonego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="6fd56-103">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

## <span data-ttu-id="6fd56-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6fd56-104">SYNTAX</span></span>

### <span data-ttu-id="6fd56-105">SetByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="6fd56-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceGroupName] <String> [-Name] <String>
 -EncryptionKeyName <String> -EncryptionKeyVersion <String> -EncryptionVaultUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fd56-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fd56-106">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceId] <String> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fd56-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fd56-107">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-InputObject] <AzureHDInsightCluster> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fd56-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6fd56-108">DESCRIPTION</span></span>
<span data-ttu-id="6fd56-109">Obróć klucz szyfrowania dysku określonego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="6fd56-109">Rotate the disk encryption key of the specified HDInsight cluster.</span></span> <span data-ttu-id="6fd56-110">W przypadku tej operacji klaster musi mieć dostęp zarówno do bieżącego, jak i zamierzonego nowego klucza, w przeciwnym razie operacja obracania klucza nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="6fd56-110">For this operation, the cluster must have access to both the current key and the intended new key, otherwise the rotate key operation will fail.</span></span>

## <span data-ttu-id="6fd56-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6fd56-111">EXAMPLES</span></span>

### <span data-ttu-id="6fd56-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6fd56-112">Example 1</span></span>
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

### <span data-ttu-id="6fd56-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6fd56-113">Example 2</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterName = "your-cmk-cluster"

$cluster= Get-AzHDInsightCluster -ClusterName $clusterName 
$cluster |  Set-AzHDInsightClusterDiskEncryptionKey `
    -EncryptionKeyName new-key `
    -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
    -EncryptionKeyVersion 00000000000000000000000000000000
```

## <span data-ttu-id="6fd56-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fd56-114">PARAMETERS</span></span>

### <span data-ttu-id="6fd56-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fd56-115">-DefaultProfile</span></span>
<span data-ttu-id="6fd56-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6fd56-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fd56-117">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="6fd56-117">-EncryptionKeyName</span></span>
<span data-ttu-id="6fd56-118">Pobiera lub ustawia nazwę klucza szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="6fd56-118">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="6fd56-119">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="6fd56-119">-EncryptionKeyVersion</span></span>
<span data-ttu-id="6fd56-120">Pobiera lub ustawia wersję klucza szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="6fd56-120">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="6fd56-121">- EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="6fd56-121">-EncryptionVaultUri</span></span>
<span data-ttu-id="6fd56-122">Pobiera lub ustawia uri magazynu szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="6fd56-122">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="6fd56-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fd56-123">-InputObject</span></span>
<span data-ttu-id="6fd56-124">Pobiera lub ustawia obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="6fd56-124">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="6fd56-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6fd56-125">-Name</span></span>
<span data-ttu-id="6fd56-126">Pobiera lub ustawia nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="6fd56-126">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="6fd56-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fd56-127">-ResourceGroupName</span></span>
<span data-ttu-id="6fd56-128">Pobiera lub ustawia nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6fd56-128">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="6fd56-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fd56-129">-ResourceId</span></span>
<span data-ttu-id="6fd56-130">Pobiera lub ustawia identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="6fd56-130">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="6fd56-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6fd56-131">-Confirm</span></span>
<span data-ttu-id="6fd56-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6fd56-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fd56-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fd56-133">-WhatIf</span></span>
<span data-ttu-id="6fd56-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fd56-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6fd56-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6fd56-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fd56-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fd56-136">CommonParameters</span></span>
<span data-ttu-id="6fd56-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fd56-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fd56-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6fd56-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fd56-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fd56-139">INPUTS</span></span>

### <span data-ttu-id="6fd56-140">Brak</span><span class="sxs-lookup"><span data-stu-id="6fd56-140">None</span></span>

## <span data-ttu-id="6fd56-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fd56-141">OUTPUTS</span></span>

### <span data-ttu-id="6fd56-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span><span class="sxs-lookup"><span data-stu-id="6fd56-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="6fd56-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6fd56-143">NOTES</span></span>

## <span data-ttu-id="6fd56-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6fd56-144">RELATED LINKS</span></span>

[<span data-ttu-id="6fd56-145">Szyfrowanie dysków zarządzane przez klienta</span><span class="sxs-lookup"><span data-stu-id="6fd56-145">Customer-managed key disk encryption</span></span>](https://docs.microsoft.com/azure/hdinsight/disk-encryption)
