---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 2a9c2870e0ce33b93d3013e84e7de3642b42708c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185419"
---
# <span data-ttu-id="0a61b-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="0a61b-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="0a61b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a61b-102">SYNOPSIS</span></span>
<span data-ttu-id="0a61b-103">Zaktualizuj stan magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0a61b-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="0a61b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0a61b-104">SYNTAX</span></span>

### <span data-ttu-id="0a61b-105">UpdateByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="0a61b-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a61b-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a61b-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a61b-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a61b-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a61b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0a61b-108">DESCRIPTION</span></span>
<span data-ttu-id="0a61b-109">To polecenie cmdlet aktualizuje stan magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0a61b-109">This cmdlet updates the state of an Azure key vault.</span></span>

## <span data-ttu-id="0a61b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0a61b-110">EXAMPLES</span></span>

### <span data-ttu-id="0a61b-111">Przykład 1. Włączanie ochrony przed przeczyszczaniami</span><span class="sxs-lookup"><span data-stu-id="0a61b-111">Example 1： Enable purge protection</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="0a61b-112">Zapewnia ochronę przed przeczyszczaniami przy użyciu składni połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="0a61b-112">Enables purge protection using piping syntax.</span></span>

### <span data-ttu-id="0a61b-113">Przykład 2. Włączanie autoryzacji RBAC</span><span class="sxs-lookup"><span data-stu-id="0a61b-113">Example 2： Enable RBAC Authorization</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnableRbacAuthorization $true
```

<span data-ttu-id="0a61b-114">Umożliwia autoryzację RBAC przy użyciu składni połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="0a61b-114">Enables RBAC Authorization using piping syntax.</span></span>

### <span data-ttu-id="0a61b-115">Przykład 3. Ustawianie tagów</span><span class="sxs-lookup"><span data-stu-id="0a61b-115">Example 3： Set tags</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName | Update-AzKeyVault -Tags @{key = "value"}
```

<span data-ttu-id="0a61b-116">Ustawia tagi magazynu kluczy o nazwie $keyVaultName.</span><span class="sxs-lookup"><span data-stu-id="0a61b-116">Sets the tags of a key vault named $keyVaultName.</span></span>

### <span data-ttu-id="0a61b-117">Przykład 4. Czyszczenie tagów</span><span class="sxs-lookup"><span data-stu-id="0a61b-117">Example 4： Clean tags</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName | Update-AzKeyVault -Tags @{}
```

<span data-ttu-id="0a61b-118">Usuwa wszystkie tagi magazynu kluczy o nazwie $keyVaultName.</span><span class="sxs-lookup"><span data-stu-id="0a61b-118">Deletes all tags of a key vault named $keyVaultName.</span></span>

## <span data-ttu-id="0a61b-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a61b-119">PARAMETERS</span></span>

### <span data-ttu-id="0a61b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a61b-120">-DefaultProfile</span></span>
<span data-ttu-id="0a61b-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0a61b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a61b-122">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="0a61b-122">-EnablePurgeProtection</span></span>
<span data-ttu-id="0a61b-123">Włącz funkcję ochrony przed przeczyszczaniami dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="0a61b-123">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="0a61b-124">Po włączeniu tej funkcji nie można jej wyłączyć.</span><span class="sxs-lookup"><span data-stu-id="0a61b-124">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="0a61b-125">Wymaga ona miękkiego usunięcia, aby została włączona.</span><span class="sxs-lookup"><span data-stu-id="0a61b-125">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="0a61b-126">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="0a61b-126">-EnableRbacAuthorization</span></span>
<span data-ttu-id="0a61b-127">Włącz lub wyłącz ten magazyn kluczy, aby autoryzować akcje danych za pomocą kontroli dostępu opartej na rolach (RBAC, Role Based Access Control).</span><span class="sxs-lookup"><span data-stu-id="0a61b-127">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

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

### <span data-ttu-id="0a61b-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a61b-128">-InputObject</span></span>
<span data-ttu-id="0a61b-129">Obiekt magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="0a61b-129">Key vault object.</span></span>

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

### <span data-ttu-id="0a61b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a61b-130">-ResourceGroupName</span></span>
<span data-ttu-id="0a61b-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0a61b-131">Name of the resource group.</span></span>

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

### <span data-ttu-id="0a61b-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a61b-132">-ResourceId</span></span>
<span data-ttu-id="0a61b-133">Identyfikator zasobu magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="0a61b-133">Resource ID of the key vault.</span></span>

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

### <span data-ttu-id="0a61b-134">— Tag</span><span class="sxs-lookup"><span data-stu-id="0a61b-134">-Tag</span></span>
<span data-ttu-id="0a61b-135">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="0a61b-135">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a61b-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0a61b-136">-VaultName</span></span>
<span data-ttu-id="0a61b-137">Nazwa magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="0a61b-137">Name of the key vault.</span></span>

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

### <span data-ttu-id="0a61b-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0a61b-138">-Confirm</span></span>
<span data-ttu-id="0a61b-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0a61b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a61b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a61b-140">-WhatIf</span></span>
<span data-ttu-id="0a61b-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a61b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a61b-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0a61b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a61b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a61b-143">CommonParameters</span></span>
<span data-ttu-id="0a61b-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a61b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a61b-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a61b-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a61b-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a61b-146">INPUTS</span></span>

### <span data-ttu-id="0a61b-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="0a61b-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="0a61b-148">System.String</span><span class="sxs-lookup"><span data-stu-id="0a61b-148">System.String</span></span>

## <span data-ttu-id="0a61b-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0a61b-149">OUTPUTS</span></span>

### <span data-ttu-id="0a61b-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="0a61b-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="0a61b-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0a61b-151">NOTES</span></span>

## <span data-ttu-id="0a61b-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a61b-152">RELATED LINKS</span></span>
