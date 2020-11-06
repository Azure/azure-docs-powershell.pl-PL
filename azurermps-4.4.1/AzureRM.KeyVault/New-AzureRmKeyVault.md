---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://go.microsoft.com/fwlink/?LinkId=690160
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
ms.openlocfilehash: 28cd93fe9de14365e4de626729ec45a7aaa88cdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553855"
---
# <span data-ttu-id="b7b9a-101">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="b7b9a-101">New-AzureRmKeyVault</span></span>

## <span data-ttu-id="b7b9a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7b9a-102">SYNOPSIS</span></span>
<span data-ttu-id="b7b9a-103">Tworzy magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-103">Creates a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7b9a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7b9a-104">SYNTAX</span></span>

```
New-AzureRmKeyVault [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7b9a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b7b9a-105">DESCRIPTION</span></span>
<span data-ttu-id="b7b9a-106">Polecenie cmdlet **New-AzureRmKeyVault** tworzy magazyn kluczy w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-106">The **New-AzureRmKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="b7b9a-107">To polecenie cmdlet udziela również uprawnień do aktualnie zalogowanego użytkownika w celu dodawania, usuwania lub list kluczy i sekretów w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>

<span data-ttu-id="b7b9a-108">Uwaga: Jeśli zobaczysz błąd **, subskrypcja nie jest zarejestrowana w celu użycia obszaru nazw "Microsoft.** DataTable" podczas próby utworzenia nowego magazynu kluczy Uruchom polecenie **register-AzureRmResourceProvider-ProviderNamespace "Microsoft.** Keying", a następnie uruchom polecenie **New-AzureRmKeyVault** .</span><span class="sxs-lookup"><span data-stu-id="b7b9a-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzureRmKeyVault** command.</span></span> <span data-ttu-id="b7b9a-109">Aby uzyskać więcej informacji, zobacz Register-AzureRmResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-109">For more information, see Register-AzureRmResourceProvider.</span></span>

## <span data-ttu-id="b7b9a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7b9a-110">EXAMPLES</span></span>

### <span data-ttu-id="b7b9a-111">Przykład 1. Tworzenie standardowego magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="b7b9a-111">Example 1: Create a Standard key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

<span data-ttu-id="b7b9a-112">To polecenie tworzy magazyn kluczy o nazwie Contoso03Vault w obszarze Azure wschodniego USA.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="b7b9a-113">Polecenie dodaje Magazyn kluczy do grupy zasobów o nazwie Group14.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="b7b9a-114">Ponieważ polecenie nie określa wartości parametru *SKU* , tworzy on standardowy magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="b7b9a-115">Przykład 2: Tworzenie dużego magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="b7b9a-115">Example 2: Create a Premium key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'
```

<span data-ttu-id="b7b9a-116">To polecenie tworzy magazyn kluczy, podobnie jak w poprzednim przykładzie.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="b7b9a-117">Jednak określa wartość Premium dla parametru *SKU* w celu utworzenia magazynu kluczy Premium.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="b7b9a-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7b9a-118">PARAMETERS</span></span>

### <span data-ttu-id="b7b9a-119">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="b7b9a-119">-EnabledForDeployment</span></span>
<span data-ttu-id="b7b9a-120">Umożliwia dostawcy zasobów Microsoft. COMPUTE na pobieranie kluczy tajnych z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się tworzenie zasobów, na przykład podczas tworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-120">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7b9a-121">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="b7b9a-121">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="b7b9a-122">Umożliwia usłudze szyfrowania dysków Azure uzyskiwanie kluczy tajnych i ich odwinięcie z tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-122">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7b9a-123">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="b7b9a-123">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="b7b9a-124">Umożliwia menedżerowi zasobów platformy Azure pobieranie kluczy tajnych z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się wdrożenie szablonu.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-124">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7b9a-125">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="b7b9a-125">-EnableSoftDelete</span></span>
<span data-ttu-id="b7b9a-126">Jeśli ta opcja jest określona, funkcja "Soft Delete" jest włączona dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-126">If specified, 'soft delete' functionality is enabled for this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7b9a-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b7b9a-127">-Location</span></span>
<span data-ttu-id="b7b9a-128">Określa obszar Azure, w którym ma zostać utworzony magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-128">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="b7b9a-129">Użyj polecenia Get-AzureLocation ( https://msdn.microsoft.com/ Library/Azure/mt589064. aspx), aby wyświetlić dostępne opcje.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-129">Use the command Get-AzureLocation (https://msdn.microsoft.com/ library/azure/mt589064.aspx) to see your choices.</span></span> <span data-ttu-id="b7b9a-130">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-AzureLocation` .</span><span class="sxs-lookup"><span data-stu-id="b7b9a-130">For more information, type `Get-Help Get-AzureLocation`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7b9a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7b9a-131">-ResourceGroupName</span></span>
<span data-ttu-id="b7b9a-132">Określa nazwę istniejącej grupy zasobów, w której ma zostać utworzony magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="b7b9a-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="b7b9a-133">-Sku</span></span>
<span data-ttu-id="b7b9a-134">Określa jednostkę SKU wystąpienia magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-134">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="b7b9a-135">Aby uzyskać informacje o tym, jakie funkcje są dostępne dla poszczególnych wersji SKU, zobacz witrynę sieci Web usługi Azure Key (cennik) https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="b7b9a-135">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: Microsoft.Azure.Management.KeyVault.Models.SkuName
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7b9a-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="b7b9a-136">-Tag</span></span>
<span data-ttu-id="b7b9a-137">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b7b9a-138">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="b7b9a-138">For example:</span></span>

<span data-ttu-id="b7b9a-139">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="b7b9a-139">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b7b9a-140">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="b7b9a-140">-VaultName</span></span>
<span data-ttu-id="b7b9a-141">Określa nazwę magazynu kluczy, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-141">Specifies the name of the key vault to create.</span></span> <span data-ttu-id="b7b9a-142">Nazwa może być dowolną kombinacją liter, cyfr lub łączników.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-142">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="b7b9a-143">Nazwa musi zaczynać się i kończyć literą lub cyfrą.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-143">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="b7b9a-144">Nazwa musi być uniwersalnie unikatowa.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-144">The name must be universally unique.</span></span>

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

### <span data-ttu-id="b7b9a-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b7b9a-145">-Confirm</span></span>
<span data-ttu-id="b7b9a-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7b9a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7b9a-147">-WhatIf</span></span>
<span data-ttu-id="b7b9a-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7b9a-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7b9a-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7b9a-150">-DefaultProfile</span></span>
<span data-ttu-id="b7b9a-151">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7b9a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7b9a-152">CommonParameters</span></span>
<span data-ttu-id="b7b9a-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7b9a-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7b9a-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7b9a-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7b9a-155">INPUTS</span></span>

## <span data-ttu-id="b7b9a-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7b9a-156">OUTPUTS</span></span>

### <span data-ttu-id="b7b9a-157">Microsoft. Azure. Commands. platforming. models. PSVault</span><span class="sxs-lookup"><span data-stu-id="b7b9a-157">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="b7b9a-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7b9a-158">NOTES</span></span>

## <span data-ttu-id="b7b9a-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7b9a-159">RELATED LINKS</span></span>

[<span data-ttu-id="b7b9a-160">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="b7b9a-160">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="b7b9a-161">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="b7b9a-161">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
