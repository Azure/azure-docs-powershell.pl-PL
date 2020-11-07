---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-Azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 41fcea2b0afc7c18da2f3e4e71764bff1ab2920c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893041"
---
# <span data-ttu-id="598af-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="598af-101">New-AzKeyVault</span></span>

## <span data-ttu-id="598af-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="598af-102">SYNOPSIS</span></span>
<span data-ttu-id="598af-103">Tworzy magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="598af-103">Creates a key vault.</span></span>

## <span data-ttu-id="598af-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="598af-104">SYNTAX</span></span>

```
New-AzKeyVault [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="598af-105">Opis</span><span class="sxs-lookup"><span data-stu-id="598af-105">DESCRIPTION</span></span>
<span data-ttu-id="598af-106">Polecenie cmdlet **New-AzKeyVault** tworzy magazyn kluczy w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="598af-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="598af-107">To polecenie cmdlet udziela również uprawnień do aktualnie zalogowanego użytkownika w celu dodawania, usuwania lub list kluczy i sekretów w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="598af-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>

<span data-ttu-id="598af-108">Uwaga: Jeśli zobaczysz błąd **, subskrypcja nie jest zarejestrowana w celu użycia obszaru nazw "Microsoft.** DataTable" podczas próby utworzenia nowego magazynu kluczy Uruchom polecenie **register-AzResourceProvider-ProviderNamespace "Microsoft.** Keying", a następnie uruchom polecenie **New-AzKeyVault** .</span><span class="sxs-lookup"><span data-stu-id="598af-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="598af-109">Aby uzyskać więcej informacji, zobacz Register-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="598af-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="598af-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="598af-110">EXAMPLES</span></span>

### <span data-ttu-id="598af-111">Przykład 1. Tworzenie standardowego magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="598af-111">Example 1: Create a Standard key vault</span></span>
```
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

<span data-ttu-id="598af-112">To polecenie tworzy magazyn kluczy o nazwie Contoso03Vault w obszarze Azure wschodniego USA.</span><span class="sxs-lookup"><span data-stu-id="598af-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="598af-113">Polecenie dodaje Magazyn kluczy do grupy zasobów o nazwie Group14.</span><span class="sxs-lookup"><span data-stu-id="598af-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="598af-114">Ponieważ polecenie nie określa wartości parametru *SKU* , tworzy on standardowy magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="598af-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="598af-115">Przykład 2: Tworzenie dużego magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="598af-115">Example 2: Create a Premium key vault</span></span>
```
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'
```

<span data-ttu-id="598af-116">To polecenie tworzy magazyn kluczy, podobnie jak w poprzednim przykładzie.</span><span class="sxs-lookup"><span data-stu-id="598af-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="598af-117">Jednak określa wartość Premium dla parametru *SKU* w celu utworzenia magazynu kluczy Premium.</span><span class="sxs-lookup"><span data-stu-id="598af-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="598af-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="598af-118">PARAMETERS</span></span>

### <span data-ttu-id="598af-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="598af-119">-DefaultProfile</span></span>
<span data-ttu-id="598af-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="598af-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="598af-121">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="598af-121">-EnabledForDeployment</span></span>
<span data-ttu-id="598af-122">Umożliwia dostawcy zasobów Microsoft. COMPUTE na pobieranie kluczy tajnych z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się tworzenie zasobów, na przykład podczas tworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="598af-122">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="598af-123">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="598af-123">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="598af-124">Umożliwia usłudze szyfrowania dysków Azure uzyskiwanie kluczy tajnych i ich odwinięcie z tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="598af-124">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="598af-125">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="598af-125">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="598af-126">Umożliwia menedżerowi zasobów platformy Azure pobieranie kluczy tajnych z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się wdrożenie szablonu.</span><span class="sxs-lookup"><span data-stu-id="598af-126">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="598af-127">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="598af-127">-EnableSoftDelete</span></span>
<span data-ttu-id="598af-128">Określa, że funkcja soft-DELETE jest włączona dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="598af-128">Specifies that the soft-delete functionality is enabled for this key vault.</span></span> <span data-ttu-id="598af-129">Jeśli funkcja usuwania nietrwałego jest włączona, w okresie prolongaty możesz odzyskać ten magazyn kluczy wraz z jego zawartością po jego usunięciu.</span><span class="sxs-lookup"><span data-stu-id="598af-129">When soft-delete is enabled, for a grace period, you can recover this key vault and its contents after it is deleted.</span></span>

<span data-ttu-id="598af-130">Aby uzyskać więcej informacji na temat tej funkcji, zobacz programowy [Magazyn kluczy Azure — omówienie usuwania](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span><span class="sxs-lookup"><span data-stu-id="598af-130">For more information about this functionality, see [Azure Key Vault soft-delete overview](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span></span> <span data-ttu-id="598af-131">Aby uzyskać instrukcje, zobacz [Korzystanie z programu PowerShell w celu korzystania z magazynu kluczy](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span><span class="sxs-lookup"><span data-stu-id="598af-131">For how-to instructions, see [How to use Key Vault soft-delete with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="598af-132">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="598af-132">-Location</span></span>
<span data-ttu-id="598af-133">Określa obszar Azure, w którym ma zostać utworzony magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="598af-133">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="598af-134">Użyj polecenia [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) , aby wyświetlić wybrane opcje.</span><span class="sxs-lookup"><span data-stu-id="598af-134">Use the command [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) to see your choices.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="598af-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="598af-135">-ResourceGroupName</span></span>
<span data-ttu-id="598af-136">Określa nazwę istniejącej grupy zasobów, w której ma zostać utworzony magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="598af-136">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="598af-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="598af-137">-Sku</span></span>
<span data-ttu-id="598af-138">Określa jednostkę SKU wystąpienia magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="598af-138">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="598af-139">Aby uzyskać informacje o tym, jakie funkcje są dostępne dla poszczególnych wersji SKU, zobacz witrynę sieci Web usługi Azure Key (cennik) https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="598af-139">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: SkuName
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="598af-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="598af-140">-Tag</span></span>
<span data-ttu-id="598af-141">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="598af-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="598af-142">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="598af-142">For example:</span></span>

<span data-ttu-id="598af-143">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="598af-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="598af-144">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="598af-144">-VaultName</span></span>
<span data-ttu-id="598af-145">Określa nazwę magazynu kluczy, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="598af-145">Specifies the name of the key vault to create.</span></span> <span data-ttu-id="598af-146">Nazwa może być dowolną kombinacją liter, cyfr lub łączników.</span><span class="sxs-lookup"><span data-stu-id="598af-146">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="598af-147">Nazwa musi zaczynać się i kończyć literą lub cyfrą.</span><span class="sxs-lookup"><span data-stu-id="598af-147">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="598af-148">Nazwa musi być uniwersalnie unikatowa.</span><span class="sxs-lookup"><span data-stu-id="598af-148">The name must be universally unique.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="598af-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="598af-149">-Confirm</span></span>
<span data-ttu-id="598af-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="598af-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="598af-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="598af-151">-WhatIf</span></span>
<span data-ttu-id="598af-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="598af-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="598af-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="598af-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="598af-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="598af-154">CommonParameters</span></span>
<span data-ttu-id="598af-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="598af-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="598af-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="598af-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="598af-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="598af-157">INPUTS</span></span>

### <span data-ttu-id="598af-158">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="598af-158">None</span></span>
<span data-ttu-id="598af-159">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="598af-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="598af-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="598af-160">OUTPUTS</span></span>

### <span data-ttu-id="598af-161">Microsoft. Azure. Commands. platforming. models. PSVault</span><span class="sxs-lookup"><span data-stu-id="598af-161">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="598af-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="598af-162">NOTES</span></span>

## <span data-ttu-id="598af-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="598af-163">RELATED LINKS</span></span>

[<span data-ttu-id="598af-164">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="598af-164">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="598af-165">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="598af-165">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
