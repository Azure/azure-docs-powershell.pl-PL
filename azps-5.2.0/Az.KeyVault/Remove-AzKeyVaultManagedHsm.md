---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 82521bd7d0ff4f34f68029cdb7faacdd198f2b02
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335641"
---
# <span data-ttu-id="26c26-101">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="26c26-101">Remove-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="26c26-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26c26-102">SYNOPSIS</span></span>
<span data-ttu-id="26c26-103">Usuwa zarządzany element HSM.</span><span class="sxs-lookup"><span data-stu-id="26c26-103">Deletes a managed HSM.</span></span>

## <span data-ttu-id="26c26-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26c26-104">SYNTAX</span></span>

### <span data-ttu-id="26c26-105">RemoveManagedHsmByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="26c26-105">RemoveManagedHsmByName (Default)</span></span>
```
Remove-AzKeyVaultManagedHsm [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26c26-106">RemoveManagedHsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="26c26-106">RemoveManagedHsmByInputObject</span></span>
```
Remove-AzKeyVaultManagedHsm [-InputObject] <PSManagedHsm> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26c26-107">RemoveManagedHsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="26c26-107">RemoveManagedHsmByResourceId</span></span>
```
Remove-AzKeyVaultManagedHsm [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26c26-108">Opis</span><span class="sxs-lookup"><span data-stu-id="26c26-108">DESCRIPTION</span></span>
<span data-ttu-id="26c26-109">Polecenie cmdlet **Remove-AzKeyVaultManagedHsm** umożliwia usunięcie określonego zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="26c26-109">The **Remove-AzKeyVaultManagedHsm** cmdlet deletes the specified managed HSM.</span></span>
<span data-ttu-id="26c26-110">Usuwa również wszystkie klucze zawarte w tym wystąpieniu.</span><span class="sxs-lookup"><span data-stu-id="26c26-110">It also deletes all keys contained in that instance.</span></span>
<span data-ttu-id="26c26-111">Pamiętaj, że chociaż określenie grupy zasobów jest opcjonalne dla tego polecenia cmdlet, należy zapewnić lepszą wydajność.</span><span class="sxs-lookup"><span data-stu-id="26c26-111">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="26c26-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26c26-112">EXAMPLES</span></span>

### <span data-ttu-id="26c26-113">Przykład 1: usuwanie zarządzanego modułu HSM</span><span class="sxs-lookup"><span data-stu-id="26c26-113">Example 1: Remove a managed HSM</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -Force

True
```

<span data-ttu-id="26c26-114">To polecenie powoduje usunięcie zarządzanego modułu HSM o nazwie myhsm z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="26c26-114">This command removes the managed hsm named myhsm from your current subscription.</span></span>

### <span data-ttu-id="26c26-115">Przykład 2: usuwanie zarządzanego modułu HSM z określonej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="26c26-115">Example 2: Remove a managed hsm from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -ResourceGroupName "myrg1" -PassThru

True
```

<span data-ttu-id="26c26-116">To polecenie powoduje usunięcie zarządzanego modułu HSM o nazwie myhsm z grupy zasobów o nazwie myrg1.</span><span class="sxs-lookup"><span data-stu-id="26c26-116">This command removes the managed hsm named myhsm from the resource group named myrg1.</span></span>
<span data-ttu-id="26c26-117">Jeśli nazwa grupy zasobów nie zostanie określona, polecenie cmdlet wyszukuje nazwa zarządzanego modułu HSM, który ma zostać usunięty z bieżącego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="26c26-117">If you do not specify the resource group name, the cmdlet searches for the named managed HSM to delete in your current subscription.</span></span>

## <span data-ttu-id="26c26-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26c26-118">PARAMETERS</span></span>

### <span data-ttu-id="26c26-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26c26-119">-AsJob</span></span>
<span data-ttu-id="26c26-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="26c26-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26c26-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26c26-121">-DefaultProfile</span></span>
<span data-ttu-id="26c26-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="26c26-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26c26-123">-Force</span><span class="sxs-lookup"><span data-stu-id="26c26-123">-Force</span></span>
<span data-ttu-id="26c26-124">Wskazuje, że polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="26c26-124">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="26c26-125">Domyślnie to polecenie cmdlet monituje o potwierdzenie zamiaru usunięcia zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="26c26-125">By default, this cmdlet prompts you to confirm that you want to delete the managed HSM.</span></span>

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

### <span data-ttu-id="26c26-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="26c26-126">-InputObject</span></span>
<span data-ttu-id="26c26-127">Obiekt zarządzanego modułu HSM, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="26c26-127">Managed HSM object to be deleted.</span></span>

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

### <span data-ttu-id="26c26-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="26c26-128">-Name</span></span>
<span data-ttu-id="26c26-129">Określa nazwę zarządzanego modułu HSM, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="26c26-129">Specifies the name of the managed HSM to remove.</span></span>

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

### <span data-ttu-id="26c26-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26c26-130">-PassThru</span></span>
<span data-ttu-id="26c26-131">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="26c26-131">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="26c26-132">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="26c26-132">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="26c26-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26c26-133">-ResourceGroupName</span></span>
<span data-ttu-id="26c26-134">Określa nazwę grupy zasobów dla modułu HSM zarządzanego platformy Azure do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="26c26-134">Specifies the name of resource group for Azure managed HSM to remove.</span></span>

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

### <span data-ttu-id="26c26-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26c26-135">-ResourceId</span></span>
<span data-ttu-id="26c26-136">Identyfikator zasobu ManagedHsm.</span><span class="sxs-lookup"><span data-stu-id="26c26-136">ManagedHsm Resource Id.</span></span>

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

### <span data-ttu-id="26c26-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="26c26-137">-Confirm</span></span>
<span data-ttu-id="26c26-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26c26-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26c26-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26c26-139">-WhatIf</span></span>
<span data-ttu-id="26c26-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26c26-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26c26-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="26c26-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26c26-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26c26-142">CommonParameters</span></span>
<span data-ttu-id="26c26-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26c26-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26c26-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26c26-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26c26-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26c26-145">INPUTS</span></span>

### <span data-ttu-id="26c26-146">Microsoft. Azure. Commands. platforming. models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="26c26-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="26c26-147">System. String</span><span class="sxs-lookup"><span data-stu-id="26c26-147">System.String</span></span>

## <span data-ttu-id="26c26-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26c26-148">OUTPUTS</span></span>

### <span data-ttu-id="26c26-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26c26-149">System.Boolean</span></span>

## <span data-ttu-id="26c26-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26c26-150">NOTES</span></span>

## <span data-ttu-id="26c26-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26c26-151">RELATED LINKS</span></span>

[<span data-ttu-id="26c26-152">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="26c26-152">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="26c26-153">Nowe — AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="26c26-153">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="26c26-154">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="26c26-154">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)