---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 69a1155b99d054699c41cc0b26cd78ef4445f931
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503477"
---
# <span data-ttu-id="10ba1-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="10ba1-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="10ba1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="10ba1-102">SYNOPSIS</span></span>
<span data-ttu-id="10ba1-103">Usuwa Magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="10ba1-103">Deletes a key vault.</span></span>

## <span data-ttu-id="10ba1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="10ba1-104">SYNTAX</span></span>

### <span data-ttu-id="10ba1-105">ByAvailableVault (domyślny)</span><span class="sxs-lookup"><span data-stu-id="10ba1-105">ByAvailableVault (Default)</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10ba1-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="10ba1-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10ba1-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="10ba1-107">InputObjectByAvailableVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10ba1-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="10ba1-108">InputObjectByDeletedVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10ba1-109">ResourceIdByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="10ba1-109">ResourceIdByAvailableVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10ba1-110">ResourceIdByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="10ba1-110">ResourceIdByDeletedVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10ba1-111">Opis</span><span class="sxs-lookup"><span data-stu-id="10ba1-111">DESCRIPTION</span></span>
<span data-ttu-id="10ba1-112">Polecenie cmdlet **Remove-AzKeyVault** usuwa określony magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="10ba1-112">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="10ba1-113">Usuwane są również wszystkie klucze i klucze tajne zawarte w tym wystąpieniu.</span><span class="sxs-lookup"><span data-stu-id="10ba1-113">It also deletes all keys and secrets contained in that instance.</span></span>
<span data-ttu-id="10ba1-114">Pamiętaj, że chociaż określenie grupy zasobów jest opcjonalne dla tego polecenia cmdlet, należy zapewnić lepszą wydajność.</span><span class="sxs-lookup"><span data-stu-id="10ba1-114">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="10ba1-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="10ba1-115">EXAMPLES</span></span>

### <span data-ttu-id="10ba1-116">Przykład 1: Usuwanie magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="10ba1-116">Example 1: Remove a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

<span data-ttu-id="10ba1-117">To polecenie usuwa Magazyn kluczy o nazwie Contoso03Vault z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="10ba1-117">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="10ba1-118">Przykład 2: Usuwanie magazynu kluczy z określonej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="10ba1-118">Example 2: Remove a key vault from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVault -Name "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

<span data-ttu-id="10ba1-119">To polecenie usuwa Magazyn kluczy o nazwie Contoso03Vault z grupy nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="10ba1-119">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="10ba1-120">Jeśli nazwa grupy zasobów nie zostanie określona, polecenie cmdlet wyszukuje w bieżącym abonamentie nazwany Magazyn kluczy, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="10ba1-120">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

### <span data-ttu-id="10ba1-121">Przykład 3: usuwanie zarządzanego modułu HSM</span><span class="sxs-lookup"><span data-stu-id="10ba1-121">Example 3: Remove a managed hsm</span></span>
```powershell
PS C:\>  Remove-AzKeyVault -Name "testManagedHsm" -Hsm -PassThru

True
```

<span data-ttu-id="10ba1-122">To polecenie powoduje usunięcie zarządzanego modułu HSM o nazwie testManagedHsm z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="10ba1-122">This command removes the managed hsm named testManagedHsm from your current subscription.</span></span>

## <span data-ttu-id="10ba1-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="10ba1-123">PARAMETERS</span></span>

### <span data-ttu-id="10ba1-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10ba1-124">-AsJob</span></span>
<span data-ttu-id="10ba1-125">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="10ba1-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10ba1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10ba1-126">-DefaultProfile</span></span>
<span data-ttu-id="10ba1-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="10ba1-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10ba1-128">-Force</span><span class="sxs-lookup"><span data-stu-id="10ba1-128">-Force</span></span>
<span data-ttu-id="10ba1-129">Wskazuje, że polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="10ba1-129">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="10ba1-130">Domyślnie to polecenie cmdlet monituje o potwierdzenie zamiaru usunięcia magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="10ba1-130">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="10ba1-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="10ba1-131">-InputObject</span></span>
<span data-ttu-id="10ba1-132">Obiekt magazynu kluczy, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="10ba1-132">Key Vault object to be deleted.</span></span>

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

### <span data-ttu-id="10ba1-133">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="10ba1-133">-InRemovedState</span></span>
<span data-ttu-id="10ba1-134">Trwale Usuń magazyn już usunięty.</span><span class="sxs-lookup"><span data-stu-id="10ba1-134">Remove the previously deleted vault permanently.</span></span>

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

### <span data-ttu-id="10ba1-135">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="10ba1-135">-Location</span></span>
<span data-ttu-id="10ba1-136">Lokalizacja usuniętego magazynu.</span><span class="sxs-lookup"><span data-stu-id="10ba1-136">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="10ba1-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10ba1-137">-PassThru</span></span>
<span data-ttu-id="10ba1-138">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="10ba1-138">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="10ba1-139">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="10ba1-139">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="10ba1-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10ba1-140">-ResourceGroupName</span></span>
<span data-ttu-id="10ba1-141">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="10ba1-141">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="10ba1-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10ba1-142">-ResourceId</span></span>
<span data-ttu-id="10ba1-143">Identyfikator zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="10ba1-143">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="10ba1-144">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="10ba1-144">-VaultName</span></span>
<span data-ttu-id="10ba1-145">Określa nazwę magazynu kluczy, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="10ba1-145">Specifies the name of the key vault to remove.</span></span>

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

### <span data-ttu-id="10ba1-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="10ba1-146">-Confirm</span></span>
<span data-ttu-id="10ba1-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10ba1-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10ba1-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10ba1-148">-WhatIf</span></span>
<span data-ttu-id="10ba1-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10ba1-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10ba1-150">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10ba1-150">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10ba1-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="10ba1-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10ba1-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10ba1-152">CommonParameters</span></span>
<span data-ttu-id="10ba1-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10ba1-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10ba1-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10ba1-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10ba1-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10ba1-155">INPUTS</span></span>

### <span data-ttu-id="10ba1-156">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="10ba1-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="10ba1-157">System. String</span><span class="sxs-lookup"><span data-stu-id="10ba1-157">System.String</span></span>

## <span data-ttu-id="10ba1-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="10ba1-158">OUTPUTS</span></span>

### <span data-ttu-id="10ba1-159">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="10ba1-159">System.Boolean</span></span>

## <span data-ttu-id="10ba1-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="10ba1-160">NOTES</span></span>

## <span data-ttu-id="10ba1-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10ba1-161">RELATED LINKS</span></span>

[<span data-ttu-id="10ba1-162">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="10ba1-162">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="10ba1-163">Nowe — AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="10ba1-163">New-AzKeyVault</span></span>](./New-AzKeyVault.md)
