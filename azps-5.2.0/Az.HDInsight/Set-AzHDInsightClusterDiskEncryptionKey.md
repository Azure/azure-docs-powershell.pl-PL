---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5141D84C-3C58-42B9-890F-C3C9049BC1C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
ms.openlocfilehash: b3421fa4382912d11a3e3a28b81acffb7be123a2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322924"
---
# <span data-ttu-id="7d145-101">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="7d145-101">Set-AzHDInsightClusterDiskEncryptionKey</span></span>

## <span data-ttu-id="7d145-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7d145-102">SYNOPSIS</span></span>
<span data-ttu-id="7d145-103">Obraca klucz szyfrowania dysku określonego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="7d145-103">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

## <span data-ttu-id="7d145-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7d145-104">SYNTAX</span></span>

### <span data-ttu-id="7d145-105">SetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7d145-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceGroupName] <String> [-Name] <String>
 -EncryptionKeyName <String> -EncryptionKeyVersion <String> -EncryptionVaultUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d145-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d145-106">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceId] <String> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d145-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d145-107">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-InputObject] <AzureHDInsightCluster> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d145-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7d145-108">DESCRIPTION</span></span>
<span data-ttu-id="7d145-109">Obróć klucz szyfrowania dysku określonego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="7d145-109">Rotate the disk encryption key of the specified HDInsight cluster.</span></span> <span data-ttu-id="7d145-110">W przypadku tej operacji klaster musi mieć dostęp zarówno do bieżącego klucza, jak i do zamierzonego nowego klucza, w przeciwnym razie operacja obracania klucza zakończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="7d145-110">For this operation, the cluster must have access to both the current key and the intended new key, otherwise the rotate key operation will fail.</span></span>

## <span data-ttu-id="7d145-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7d145-111">EXAMPLES</span></span>

### <span data-ttu-id="7d145-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7d145-112">Example 1</span></span>
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

### <span data-ttu-id="7d145-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7d145-113">Example 2</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterName = "your-cmk-cluster"

$cluster= Get-AzHDInsightCluster -ClusterName $clusterName 
$cluster |  Set-AzHDInsightClusterDiskEncryptionKey `
    -EncryptionKeyName new-key `
    -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
    -EncryptionKeyVersion 00000000000000000000000000000000
```

## <span data-ttu-id="7d145-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7d145-114">PARAMETERS</span></span>

### <span data-ttu-id="7d145-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d145-115">-DefaultProfile</span></span>
<span data-ttu-id="7d145-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d145-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d145-117">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="7d145-117">-EncryptionKeyName</span></span>
<span data-ttu-id="7d145-118">Pobiera lub ustawia nazwę klucza szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="7d145-118">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="7d145-119">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="7d145-119">-EncryptionKeyVersion</span></span>
<span data-ttu-id="7d145-120">Pobiera lub ustawia wersję klucza szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="7d145-120">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="7d145-121">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="7d145-121">-EncryptionVaultUri</span></span>
<span data-ttu-id="7d145-122">Pobiera lub ustawia identyfikator URI magazynu szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="7d145-122">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="7d145-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7d145-123">-InputObject</span></span>
<span data-ttu-id="7d145-124">Pobiera lub ustawia obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="7d145-124">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="7d145-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7d145-125">-Name</span></span>
<span data-ttu-id="7d145-126">Pobiera lub ustawia nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="7d145-126">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="7d145-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d145-127">-ResourceGroupName</span></span>
<span data-ttu-id="7d145-128">Pobiera lub ustawia nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7d145-128">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="7d145-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d145-129">-ResourceId</span></span>
<span data-ttu-id="7d145-130">Pobiera lub ustawia identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="7d145-130">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="7d145-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7d145-131">-Confirm</span></span>
<span data-ttu-id="7d145-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d145-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d145-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d145-133">-WhatIf</span></span>
<span data-ttu-id="7d145-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d145-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d145-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7d145-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d145-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d145-136">CommonParameters</span></span>
<span data-ttu-id="7d145-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d145-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d145-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d145-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d145-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d145-139">INPUTS</span></span>

### <span data-ttu-id="7d145-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7d145-140">None</span></span>

## <span data-ttu-id="7d145-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7d145-141">OUTPUTS</span></span>

### <span data-ttu-id="7d145-142">Microsoft. Azure. Management. HDInsight. modele. Cluster</span><span class="sxs-lookup"><span data-stu-id="7d145-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="7d145-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7d145-143">NOTES</span></span>

## <span data-ttu-id="7d145-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d145-144">RELATED LINKS</span></span>

[<span data-ttu-id="7d145-145">Szyfrowanie dysków klucza zarządzanego przez klienta</span><span class="sxs-lookup"><span data-stu-id="7d145-145">Customer-managed key disk encryption</span></span>](https://docs.microsoft.com/en-us/azure/hdinsight/disk-encryption)
