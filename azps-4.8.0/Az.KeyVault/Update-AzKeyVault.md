---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 4302f2f9c4c2d6b2c7afa879fc28e2ff4edbb592
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220667"
---
# <span data-ttu-id="a7eb1-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="a7eb1-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="a7eb1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a7eb1-102">SYNOPSIS</span></span>
<span data-ttu-id="a7eb1-103">Zaktualizuj stan magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a7eb1-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="a7eb1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a7eb1-104">SYNTAX</span></span>

### <span data-ttu-id="a7eb1-105">UpdateByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a7eb1-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-SoftDeleteRetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7eb1-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7eb1-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-SoftDeleteRetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7eb1-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7eb1-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-SoftDeleteRetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7eb1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a7eb1-108">DESCRIPTION</span></span>
<span data-ttu-id="a7eb1-109">To polecenie cmdlet aktualizuje stan magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a7eb1-109">This cmdlet updates the state of an Azure key vault.</span></span>
<span data-ttu-id="a7eb1-110">Uwaga aktualizowanie części właściwości jest akcją nieodwracalną, na przykład po włączeniu funkcji usuwania elastycznego nie można jej już wyłączyć.</span><span class="sxs-lookup"><span data-stu-id="a7eb1-110">Please note updating some of the properties is an irreversible action, for example once soft delete has been enabled, it cannot be disabled anymore.</span></span>

## <span data-ttu-id="a7eb1-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a7eb1-111">EXAMPLES</span></span>

### <span data-ttu-id="a7eb1-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a7eb1-112">Example 1</span></span>
```powershell
PS C:\> Update-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName -EnableSoftDelete
```

<span data-ttu-id="a7eb1-113">Umożliwia usuwanie miękkie w magazynie kluczy o nazwie `$keyVaultName` w grupie zasób `$resourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="a7eb1-113">Enables soft delete on the key vault named `$keyVaultName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="a7eb1-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a7eb1-114">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="a7eb1-115">Włącza ochronę przed przeczyszczaniem za pomocą składni połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="a7eb1-115">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="a7eb1-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a7eb1-116">PARAMETERS</span></span>

### <span data-ttu-id="a7eb1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7eb1-117">-DefaultProfile</span></span>
<span data-ttu-id="a7eb1-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a7eb1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7eb1-119">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="a7eb1-119">-EnablePurgeProtection</span></span>
<span data-ttu-id="a7eb1-120">Włącz funkcję zabezpieczenia przed przeczyszczaniem dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="a7eb1-120">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="a7eb1-121">Po włączeniu tej możliwości nie można jej wyłączyć.</span><span class="sxs-lookup"><span data-stu-id="a7eb1-121">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="a7eb1-122">Funkcja ta wymaga włączenia Soft-Delete.</span><span class="sxs-lookup"><span data-stu-id="a7eb1-122">It requires soft-delete to be turned on.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7eb1-123">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="a7eb1-123">-EnableRbacAuthorization</span></span>
<span data-ttu-id="a7eb1-124">Włącz lub Wyłącz ten magazyn kluczy, aby autoryzować akcje danych według kontroli dostępu opartej na rolach (RBAC).</span><span class="sxs-lookup"><span data-stu-id="a7eb1-124">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7eb1-125">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="a7eb1-125">-EnableSoftDelete</span></span>
<span data-ttu-id="a7eb1-126">Włącz funkcję usuwania nietrwałego dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="a7eb1-126">Enable the soft-delete functionality for this key vault.</span></span>
<span data-ttu-id="a7eb1-127">Po włączeniu tej możliwości nie można jej wyłączyć.</span><span class="sxs-lookup"><span data-stu-id="a7eb1-127">Once enabled it cannot be disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7eb1-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a7eb1-128">-InputObject</span></span>
<span data-ttu-id="a7eb1-129">Obiekt magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="a7eb1-129">Key vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7eb1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7eb1-130">-ResourceGroupName</span></span>
<span data-ttu-id="a7eb1-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a7eb1-131">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7eb1-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7eb1-132">-ResourceId</span></span>
<span data-ttu-id="a7eb1-133">Identyfikator zasobu magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="a7eb1-133">Resource ID of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7eb1-134">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="a7eb1-134">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="a7eb1-135">Określa, jak długo usunięte zasoby są zachowywane, oraz jak długo można przeczyścić magazyn lub obiekt w stanie usunięcia.</span><span class="sxs-lookup"><span data-stu-id="a7eb1-135">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="a7eb1-136">Wartość domyślna to 90 dni.</span><span class="sxs-lookup"><span data-stu-id="a7eb1-136">The default is 90 days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7eb1-137">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="a7eb1-137">-VaultName</span></span>
<span data-ttu-id="a7eb1-138">Nazwa magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="a7eb1-138">Name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7eb1-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a7eb1-139">-Confirm</span></span>
<span data-ttu-id="a7eb1-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7eb1-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7eb1-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7eb1-141">-WhatIf</span></span>
<span data-ttu-id="a7eb1-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7eb1-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7eb1-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a7eb1-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7eb1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7eb1-144">CommonParameters</span></span>
<span data-ttu-id="a7eb1-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7eb1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7eb1-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7eb1-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7eb1-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7eb1-147">INPUTS</span></span>

### <span data-ttu-id="a7eb1-148">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a7eb1-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="a7eb1-149">System. String</span><span class="sxs-lookup"><span data-stu-id="a7eb1-149">System.String</span></span>

## <span data-ttu-id="a7eb1-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a7eb1-150">OUTPUTS</span></span>

### <span data-ttu-id="a7eb1-151">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a7eb1-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="a7eb1-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a7eb1-152">NOTES</span></span>

## <span data-ttu-id="a7eb1-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7eb1-153">RELATED LINKS</span></span>
