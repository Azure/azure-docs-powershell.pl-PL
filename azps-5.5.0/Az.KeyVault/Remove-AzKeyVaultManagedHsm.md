---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 82521bd7d0ff4f34f68029cdb7faacdd198f2b02
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199986"
---
# <span data-ttu-id="fb74f-101">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="fb74f-101">Remove-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="fb74f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb74f-102">SYNOPSIS</span></span>
<span data-ttu-id="fb74f-103">Usuwa zarządzany moduł HSM.</span><span class="sxs-lookup"><span data-stu-id="fb74f-103">Deletes a managed HSM.</span></span>

## <span data-ttu-id="fb74f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fb74f-104">SYNTAX</span></span>

### <span data-ttu-id="fb74f-105">RemoveManagedHsmByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="fb74f-105">RemoveManagedHsmByName (Default)</span></span>
```
Remove-AzKeyVaultManagedHsm [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb74f-106">RemoveManagedHsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="fb74f-106">RemoveManagedHsmByInputObject</span></span>
```
Remove-AzKeyVaultManagedHsm [-InputObject] <PSManagedHsm> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb74f-107">RemoveManagedHsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="fb74f-107">RemoveManagedHsmByResourceId</span></span>
```
Remove-AzKeyVaultManagedHsm [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb74f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="fb74f-108">DESCRIPTION</span></span>
<span data-ttu-id="fb74f-109">Polecenie **cmdlet Remove-AzKeyVaultManagedHsm** usuwa określony zarządzany moduł HSM.</span><span class="sxs-lookup"><span data-stu-id="fb74f-109">The **Remove-AzKeyVaultManagedHsm** cmdlet deletes the specified managed HSM.</span></span>
<span data-ttu-id="fb74f-110">Usuwa też wszystkie klucze zawarte w tym wystąpieniu.</span><span class="sxs-lookup"><span data-stu-id="fb74f-110">It also deletes all keys contained in that instance.</span></span>
<span data-ttu-id="fb74f-111">Pamiętaj, że mimo że w przypadku tego polecenia cmdlet określenie grupy zasobów jest opcjonalne, należy to zrobić, aby uzyskać lepszą wydajność.</span><span class="sxs-lookup"><span data-stu-id="fb74f-111">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="fb74f-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fb74f-112">EXAMPLES</span></span>

### <span data-ttu-id="fb74f-113">Przykład 1. Usunięcie zarządzanego hsm</span><span class="sxs-lookup"><span data-stu-id="fb74f-113">Example 1: Remove a managed HSM</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -Force

True
```

<span data-ttu-id="fb74f-114">To polecenie usuwa z bieżącej subskrypcji zarządzane polecenie hsm o nazwie myhsm.</span><span class="sxs-lookup"><span data-stu-id="fb74f-114">This command removes the managed hsm named myhsm from your current subscription.</span></span>

### <span data-ttu-id="fb74f-115">Przykład 2. Usunięcie zarządzanego hsm z określonej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="fb74f-115">Example 2: Remove a managed hsm from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -ResourceGroupName "myrg1" -PassThru

True
```

<span data-ttu-id="fb74f-116">To polecenie usuwa zarządzane hsm o nazwie myhsm z grupy zasobów o nazwie myrg1.</span><span class="sxs-lookup"><span data-stu-id="fb74f-116">This command removes the managed hsm named myhsm from the resource group named myrg1.</span></span>
<span data-ttu-id="fb74f-117">Jeśli nazwa grupy zasobów nie zostanie wykreślona, polecenie cmdlet wyszuka nazwany zarządzany moduł HSM do usunięcia w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fb74f-117">If you do not specify the resource group name, the cmdlet searches for the named managed HSM to delete in your current subscription.</span></span>

## <span data-ttu-id="fb74f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb74f-118">PARAMETERS</span></span>

### <span data-ttu-id="fb74f-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="fb74f-119">-AsJob</span></span>
<span data-ttu-id="fb74f-120">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fb74f-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb74f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb74f-121">-DefaultProfile</span></span>
<span data-ttu-id="fb74f-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb74f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb74f-123">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="fb74f-123">-Force</span></span>
<span data-ttu-id="fb74f-124">Wskazuje, że polecenie cmdlet nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fb74f-124">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="fb74f-125">Domyślnie to polecenie cmdlet wyświetla monit o potwierdzenie usunięcia zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="fb74f-125">By default, this cmdlet prompts you to confirm that you want to delete the managed HSM.</span></span>

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

### <span data-ttu-id="fb74f-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb74f-126">-InputObject</span></span>
<span data-ttu-id="fb74f-127">Zarządzany obiekt HSM do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="fb74f-127">Managed HSM object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: RemoveManagedHsmByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb74f-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fb74f-128">-Name</span></span>
<span data-ttu-id="fb74f-129">Określa nazwę zarządzanego modułu HSM do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="fb74f-129">Specifies the name of the managed HSM to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByName
Aliases: HsmName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb74f-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb74f-130">-PassThru</span></span>
<span data-ttu-id="fb74f-131">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="fb74f-131">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="fb74f-132">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="fb74f-132">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="fb74f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb74f-133">-ResourceGroupName</span></span>
<span data-ttu-id="fb74f-134">Określa nazwę grupy zasobów zarządzanej przez system Azure HSM do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="fb74f-134">Specifies the name of resource group for Azure managed HSM to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb74f-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb74f-135">-ResourceId</span></span>
<span data-ttu-id="fb74f-136">Identyfikator zasobu zarządzanego zarządzania.</span><span class="sxs-lookup"><span data-stu-id="fb74f-136">ManagedHsm Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb74f-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fb74f-137">-Confirm</span></span>
<span data-ttu-id="fb74f-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fb74f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb74f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb74f-139">-WhatIf</span></span>
<span data-ttu-id="fb74f-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb74f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb74f-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fb74f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb74f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb74f-142">CommonParameters</span></span>
<span data-ttu-id="fb74f-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb74f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb74f-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb74f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb74f-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb74f-145">INPUTS</span></span>

### <span data-ttu-id="fb74f-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="fb74f-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="fb74f-147">System.String</span><span class="sxs-lookup"><span data-stu-id="fb74f-147">System.String</span></span>

## <span data-ttu-id="fb74f-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb74f-148">OUTPUTS</span></span>

### <span data-ttu-id="fb74f-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fb74f-149">System.Boolean</span></span>

## <span data-ttu-id="fb74f-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fb74f-150">NOTES</span></span>

## <span data-ttu-id="fb74f-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb74f-151">RELATED LINKS</span></span>

[<span data-ttu-id="fb74f-152">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="fb74f-152">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="fb74f-153">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="fb74f-153">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="fb74f-154">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="fb74f-154">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)