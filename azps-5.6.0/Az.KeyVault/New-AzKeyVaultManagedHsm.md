---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 72804d546869f2d003813c8e69c067ad23966fa9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001306"
---
# <span data-ttu-id="4cf9d-101">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="4cf9d-101">New-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="4cf9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cf9d-102">SYNOPSIS</span></span>
<span data-ttu-id="4cf9d-103">Tworzy zarządzany moduł HSM.</span><span class="sxs-lookup"><span data-stu-id="4cf9d-103">Creates a managed HSM.</span></span>

## <span data-ttu-id="4cf9d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4cf9d-104">SYNTAX</span></span>

```
New-AzKeyVaultManagedHsm [-Name] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Administrator] <String[]> [-Sku <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cf9d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4cf9d-105">DESCRIPTION</span></span>
<span data-ttu-id="4cf9d-106">Polecenie **cmdlet New-AzKeyVaultManagedHsm** tworzy zarządzany moduł HSM w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="4cf9d-106">The **New-AzKeyVaultManagedHsm** cmdlet creates a managed HSM in the specified resource group.</span></span> <span data-ttu-id="4cf9d-107">Aby dodać, usunąć lub dodać klucze listy w zarządzanym modelu HSM, użytkownik powinien udzielić uprawnień, dodając identyfikator użytkownika do administratora.</span><span class="sxs-lookup"><span data-stu-id="4cf9d-107">To add, remove, or list keys in the managed HSM, user should grant permissions by adding user ID to Administrator.</span></span>

## <span data-ttu-id="4cf9d-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4cf9d-108">EXAMPLES</span></span>

### <span data-ttu-id="4cf9d-109">Przykład 1. Tworzenie zarządzanego modułu HSM StandardB1</span><span class="sxs-lookup"><span data-stu-id="4cf9d-109">Example 1: Create a StandardB1 managed HSM</span></span>
```powershell
PS C:\> New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="4cf9d-110">To polecenie tworzy zarządzany moduł HSM o nazwie myhsm w lokalizacji eastus2euap.</span><span class="sxs-lookup"><span data-stu-id="4cf9d-110">This command creates a managed HSM named myhsm in the location eastus2euap.</span></span> <span data-ttu-id="4cf9d-111">To polecenie dodaje zarządzany moduł HSM do grupy zasobów o nazwie myrg1.</span><span class="sxs-lookup"><span data-stu-id="4cf9d-111">The command adds the managed HSM to the resource group named myrg1.</span></span> <span data-ttu-id="4cf9d-112">Polecenie nie określa wartości dla parametru *SKU,* dlatego tworzy Standard_B1 HSM.</span><span class="sxs-lookup"><span data-stu-id="4cf9d-112">Because the command does not specify a value for the *SKU* parameter, it creates a Standard_B1 managed HSM.</span></span>

### <span data-ttu-id="4cf9d-113">Przykład 2. Tworzenie zarządzanego modułu hsm CustomB32</span><span class="sxs-lookup"><span data-stu-id="4cf9d-113">Example 2: Create a CustomB32 managed HSM</span></span>
```powershell
PS C:\>New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" -Sku 'CustomB32'
Name  Resource Group Name Location    SKU

----  ------------------- --------    ---
myhsm myrg1               eastus2euap CustomB32
```

                      

<span data-ttu-id="4cf9d-114">To polecenie tworzy zarządzany moduł HSM, podobnie jak w poprzednim przykładzie.</span><span class="sxs-lookup"><span data-stu-id="4cf9d-114">This command creates a managed HSM, just like the previous example.</span></span> <span data-ttu-id="4cf9d-115">Określa jednak wartość parametru CustomB32 dla parametru *SKU* w celu utworzenia zarządzanego modułu HSM CustomB32.</span><span class="sxs-lookup"><span data-stu-id="4cf9d-115">However, it specifies a value of CustomB32 for the *SKU* parameter to create a CustomB32 managed HSM.</span></span>

## <span data-ttu-id="4cf9d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cf9d-116">PARAMETERS</span></span>

### <span data-ttu-id="4cf9d-117">— Administrator</span><span class="sxs-lookup"><span data-stu-id="4cf9d-117">-Administrator</span></span>
<span data-ttu-id="4cf9d-118">Identyfikator obiektu administratora początkowego dla tej zarządzanej puli HSM.</span><span class="sxs-lookup"><span data-stu-id="4cf9d-118">Initial administrator object id for this managed HSM pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cf9d-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="4cf9d-119">-AsJob</span></span>
<span data-ttu-id="4cf9d-120">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4cf9d-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4cf9d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cf9d-121">-DefaultProfile</span></span>
<span data-ttu-id="4cf9d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4cf9d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cf9d-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4cf9d-123">-Location</span></span>
<span data-ttu-id="4cf9d-124">Określa region platformy Azure, w którym ma być tworzyć magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="4cf9d-124">Specifies the Azure region in which to create the key vault.</span></span>
<span data-ttu-id="4cf9d-125">Użyj polecenia Get-AzResourceProvider z parametrem ProviderNamespace, aby wyświetlić dostępne opcje.</span><span class="sxs-lookup"><span data-stu-id="4cf9d-125">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cf9d-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4cf9d-126">-Name</span></span>
<span data-ttu-id="4cf9d-127">Określa nazwę zarządzanego modułu HSM do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="4cf9d-127">Specifies a name of the managed HSM to create.</span></span>
<span data-ttu-id="4cf9d-128">Nazwa może być dowolną kombinacją liter, cyfr lub łączników.</span><span class="sxs-lookup"><span data-stu-id="4cf9d-128">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="4cf9d-129">Nazwa musi zaczynać się i kończyć literą lub cyfrą.</span><span class="sxs-lookup"><span data-stu-id="4cf9d-129">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="4cf9d-130">Nazwa musi być unikatowa.</span><span class="sxs-lookup"><span data-stu-id="4cf9d-130">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cf9d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cf9d-131">-ResourceGroupName</span></span>
<span data-ttu-id="4cf9d-132">Określa nazwę istniejącej grupy zasobów, w której ma być tworzyć magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="4cf9d-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cf9d-133">- SKU</span><span class="sxs-lookup"><span data-stu-id="4cf9d-133">-Sku</span></span>
<span data-ttu-id="4cf9d-134">Określa wartość SKU zarządzanego wystąpienia HSM.</span><span class="sxs-lookup"><span data-stu-id="4cf9d-134">Specifies the SKU of the managed HSM instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cf9d-135">— Tag</span><span class="sxs-lookup"><span data-stu-id="4cf9d-135">-Tag</span></span>
<span data-ttu-id="4cf9d-136">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="4cf9d-136">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="4cf9d-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4cf9d-137">-Confirm</span></span>
<span data-ttu-id="4cf9d-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4cf9d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cf9d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cf9d-139">-WhatIf</span></span>
<span data-ttu-id="4cf9d-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cf9d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cf9d-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4cf9d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cf9d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cf9d-142">CommonParameters</span></span>
<span data-ttu-id="4cf9d-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cf9d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cf9d-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4cf9d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cf9d-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cf9d-145">INPUTS</span></span>

### <span data-ttu-id="4cf9d-146">System.String</span><span class="sxs-lookup"><span data-stu-id="4cf9d-146">System.String</span></span>

### <span data-ttu-id="4cf9d-147">System.String[]</span><span class="sxs-lookup"><span data-stu-id="4cf9d-147">System.String[]</span></span>

### <span data-ttu-id="4cf9d-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4cf9d-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4cf9d-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cf9d-149">OUTPUTS</span></span>

### <span data-ttu-id="4cf9d-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="4cf9d-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="4cf9d-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4cf9d-151">NOTES</span></span>

## <span data-ttu-id="4cf9d-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4cf9d-152">RELATED LINKS</span></span>

[<span data-ttu-id="4cf9d-153">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="4cf9d-153">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="4cf9d-154">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="4cf9d-154">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="4cf9d-155">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="4cf9d-155">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)