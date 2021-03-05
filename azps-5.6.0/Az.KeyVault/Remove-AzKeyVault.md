---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 04b4f6be3393eae0fba2f98c477b4174612d2b79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001265"
---
# <span data-ttu-id="e37e8-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="e37e8-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="e37e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e37e8-102">SYNOPSIS</span></span>
<span data-ttu-id="e37e8-103">Usuwa magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="e37e8-103">Deletes a key vault.</span></span>

## <span data-ttu-id="e37e8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e37e8-104">SYNTAX</span></span>

### <span data-ttu-id="e37e8-105">ByAvailableVault (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e37e8-105">ByAvailableVault (Default)</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e37e8-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="e37e8-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e37e8-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="e37e8-107">InputObjectByAvailableVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e37e8-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="e37e8-108">InputObjectByDeletedVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e37e8-109">ResourceIdByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="e37e8-109">ResourceIdByAvailableVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e37e8-110">ResourceIdByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="e37e8-110">ResourceIdByDeletedVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e37e8-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="e37e8-111">DESCRIPTION</span></span>
<span data-ttu-id="e37e8-112">Polecenie **cmdlet Remove-AzKeyVault** usuwa określony magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="e37e8-112">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="e37e8-113">Usuwa też wszystkie klucze i tajemnice zawarte w tym wystąpieniu.</span><span class="sxs-lookup"><span data-stu-id="e37e8-113">It also deletes all keys and secrets contained in that instance.</span></span>
<span data-ttu-id="e37e8-114">Pamiętaj, że mimo że w przypadku tego polecenia cmdlet określenie grupy zasobów jest opcjonalne, należy to zrobić, aby uzyskać lepszą wydajność.</span><span class="sxs-lookup"><span data-stu-id="e37e8-114">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="e37e8-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e37e8-115">EXAMPLES</span></span>

### <span data-ttu-id="e37e8-116">Przykład 1. Usuwanie magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="e37e8-116">Example 1: Remove a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

<span data-ttu-id="e37e8-117">To polecenie usuwa magazyn kluczy o nazwie Contoso03Vault z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e37e8-117">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="e37e8-118">Przykład 2. Usuwanie magazynu kluczy z określonej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e37e8-118">Example 2: Remove a key vault from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVault -Name "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

<span data-ttu-id="e37e8-119">To polecenie usuwa magazyn kluczy o nazwie Contoso03Vault z nazwanej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e37e8-119">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="e37e8-120">Jeśli nie określisz nazwy grupy zasobów, polecenie cmdlet wyszuka nazwany magazyn kluczy do usunięcia w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e37e8-120">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

### <span data-ttu-id="e37e8-121">Przykład 3. Usuwanie zarządzanego hsm</span><span class="sxs-lookup"><span data-stu-id="e37e8-121">Example 3: Remove a managed hsm</span></span>
```powershell
PS C:\>  Remove-AzKeyVault -Name "testManagedHsm" -Hsm -PassThru

True
```

<span data-ttu-id="e37e8-122">To polecenie usuwa zarządzane polecenie testManagedHsm z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e37e8-122">This command removes the managed hsm named testManagedHsm from your current subscription.</span></span>

## <span data-ttu-id="e37e8-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e37e8-123">PARAMETERS</span></span>

### <span data-ttu-id="e37e8-124">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e37e8-124">-AsJob</span></span>
<span data-ttu-id="e37e8-125">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e37e8-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e37e8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e37e8-126">-DefaultProfile</span></span>
<span data-ttu-id="e37e8-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e37e8-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e37e8-128">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="e37e8-128">-Force</span></span>
<span data-ttu-id="e37e8-129">Wskazuje, że polecenie cmdlet nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e37e8-129">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="e37e8-130">Domyślnie to polecenie cmdlet monituje o potwierdzenie usunięcia magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="e37e8-130">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="e37e8-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e37e8-131">-InputObject</span></span>
<span data-ttu-id="e37e8-132">Obiekt magazynu kluczy do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e37e8-132">Key Vault object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectByAvailableVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e37e8-133">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="e37e8-133">-InRemovedState</span></span>
<span data-ttu-id="e37e8-134">Usuń trwale poprzednio usunięty magazyn.</span><span class="sxs-lookup"><span data-stu-id="e37e8-134">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, InputObjectByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e37e8-135">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e37e8-135">-Location</span></span>
<span data-ttu-id="e37e8-136">Lokalizacja usuniętego magazynu.</span><span class="sxs-lookup"><span data-stu-id="e37e8-136">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ResourceIdByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e37e8-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e37e8-137">-PassThru</span></span>
<span data-ttu-id="e37e8-138">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="e37e8-138">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="e37e8-139">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="e37e8-139">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e37e8-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e37e8-140">-ResourceGroupName</span></span>
<span data-ttu-id="e37e8-141">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e37e8-141">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e37e8-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e37e8-142">-ResourceId</span></span>
<span data-ttu-id="e37e8-143">Identyfikator zasobu KeyVault.</span><span class="sxs-lookup"><span data-stu-id="e37e8-143">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByAvailableVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e37e8-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e37e8-144">-VaultName</span></span>
<span data-ttu-id="e37e8-145">Określa nazwę magazynu kluczy do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e37e8-145">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e37e8-146">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e37e8-146">-Confirm</span></span>
<span data-ttu-id="e37e8-147">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e37e8-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e37e8-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e37e8-148">-WhatIf</span></span>
<span data-ttu-id="e37e8-149">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e37e8-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e37e8-150">Polecenie cmdlet nie zostanie uruchomione. Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e37e8-150">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e37e8-151">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e37e8-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e37e8-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e37e8-152">CommonParameters</span></span>
<span data-ttu-id="e37e8-153">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e37e8-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e37e8-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e37e8-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e37e8-155">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e37e8-155">INPUTS</span></span>

### <span data-ttu-id="e37e8-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="e37e8-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="e37e8-157">System.String</span><span class="sxs-lookup"><span data-stu-id="e37e8-157">System.String</span></span>

## <span data-ttu-id="e37e8-158">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e37e8-158">OUTPUTS</span></span>

### <span data-ttu-id="e37e8-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e37e8-159">System.Boolean</span></span>

## <span data-ttu-id="e37e8-160">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e37e8-160">NOTES</span></span>

## <span data-ttu-id="e37e8-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e37e8-161">RELATED LINKS</span></span>

[<span data-ttu-id="e37e8-162">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="e37e8-162">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="e37e8-163">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="e37e8-163">New-AzKeyVault</span></span>](./New-AzKeyVault.md)
