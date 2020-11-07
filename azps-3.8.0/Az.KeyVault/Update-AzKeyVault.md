---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 8932402fb9e4e6b27f284313bfddc764192c5e93
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895178"
---
# <span data-ttu-id="4114c-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="4114c-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="4114c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4114c-102">SYNOPSIS</span></span>
<span data-ttu-id="4114c-103">Zaktualizuj stan magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4114c-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="4114c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4114c-104">SYNTAX</span></span>

### <span data-ttu-id="4114c-105">UpdateByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4114c-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4114c-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4114c-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4114c-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4114c-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4114c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4114c-108">DESCRIPTION</span></span>
<span data-ttu-id="4114c-109">To polecenie cmdlet aktualizuje stan magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4114c-109">This cmdlet updates the state of an Azure key vault.</span></span>
<span data-ttu-id="4114c-110">Uwaga aktualizowanie części właściwości jest akcją nieodwracalną, na przykład po włączeniu funkcji usuwania elastycznego nie można jej już wyłączyć.</span><span class="sxs-lookup"><span data-stu-id="4114c-110">Please note updating some of the properties is an irreversible action, for example once soft delete has been enabled, it cannot be disabled anymore.</span></span>

## <span data-ttu-id="4114c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4114c-111">EXAMPLES</span></span>

### <span data-ttu-id="4114c-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4114c-112">Example 1</span></span>
```powershell
PS C:\> Update-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName -EnableSoftDelete
```

<span data-ttu-id="4114c-113">Umożliwia usuwanie miękkie w magazynie kluczy o nazwie `$keyVaultName` w grupie zasób `$resourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="4114c-113">Enables soft delete on the key vault named `$keyVaultName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="4114c-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4114c-114">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="4114c-115">Włącza ochronę przed przeczyszczaniem za pomocą składni połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="4114c-115">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="4114c-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4114c-116">PARAMETERS</span></span>

### <span data-ttu-id="4114c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4114c-117">-DefaultProfile</span></span>
<span data-ttu-id="4114c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4114c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4114c-119">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="4114c-119">-EnablePurgeProtection</span></span>
<span data-ttu-id="4114c-120">Włącz funkcję zabezpieczenia przed przeczyszczaniem dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="4114c-120">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="4114c-121">Po włączeniu tej możliwości nie można jej wyłączyć.</span><span class="sxs-lookup"><span data-stu-id="4114c-121">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="4114c-122">Funkcja ta wymaga włączenia Soft-Delete.</span><span class="sxs-lookup"><span data-stu-id="4114c-122">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="4114c-123">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="4114c-123">-EnableSoftDelete</span></span>
<span data-ttu-id="4114c-124">Włącz funkcję usuwania nietrwałego dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="4114c-124">Enable the soft-delete functionality for this key vault.</span></span>
<span data-ttu-id="4114c-125">Po włączeniu tej możliwości nie można jej wyłączyć.</span><span class="sxs-lookup"><span data-stu-id="4114c-125">Once enabled it cannot be disabled.</span></span>

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

### <span data-ttu-id="4114c-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4114c-126">-InputObject</span></span>
<span data-ttu-id="4114c-127">Obiekt magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="4114c-127">Key vault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4114c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4114c-128">-ResourceGroupName</span></span>
<span data-ttu-id="4114c-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4114c-129">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4114c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4114c-130">-ResourceId</span></span>
<span data-ttu-id="4114c-131">Identyfikator zasobu magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="4114c-131">Resource ID of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4114c-132">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="4114c-132">-VaultName</span></span>
<span data-ttu-id="4114c-133">Nazwa magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="4114c-133">Name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4114c-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4114c-134">-Confirm</span></span>
<span data-ttu-id="4114c-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4114c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4114c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4114c-136">-WhatIf</span></span>
<span data-ttu-id="4114c-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4114c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4114c-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4114c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4114c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4114c-139">CommonParameters</span></span>
<span data-ttu-id="4114c-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4114c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4114c-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4114c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4114c-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4114c-142">INPUTS</span></span>

### <span data-ttu-id="4114c-143">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="4114c-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="4114c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4114c-144">System.String</span></span>

## <span data-ttu-id="4114c-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4114c-145">OUTPUTS</span></span>

### <span data-ttu-id="4114c-146">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="4114c-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="4114c-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4114c-147">NOTES</span></span>

## <span data-ttu-id="4114c-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4114c-148">RELATED LINKS</span></span>
