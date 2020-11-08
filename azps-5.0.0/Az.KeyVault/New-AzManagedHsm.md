---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsm.md
ms.openlocfilehash: 2cab0fedd31f482b2e826a02f686ec8bf651c1bb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234680"
---
# <span data-ttu-id="91708-101">New-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="91708-101">New-AzManagedHsm</span></span>

## <span data-ttu-id="91708-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="91708-102">SYNOPSIS</span></span>
<span data-ttu-id="91708-103">Tworzy zarządzany modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="91708-103">Creates a managed HSM.</span></span>

## <span data-ttu-id="91708-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="91708-104">SYNTAX</span></span>

```
New-AzManagedHsm [-Name] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Administrator] <String[]> [-Sku <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91708-105">Opis</span><span class="sxs-lookup"><span data-stu-id="91708-105">DESCRIPTION</span></span>
<span data-ttu-id="91708-106">Polecenie cmdlet **New-AzManagedHsm** umożliwia utworzenie zarządzanego modułu HSM w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="91708-106">The **New-AzManagedHsm** cmdlet creates a managed HSM in the specified resource group.</span></span> <span data-ttu-id="91708-107">Aby dodać, usunąć lub wyświetlić klucze w zarządzanym modułu HSM, użytkownik powinien udzielić uprawnień, dodając identyfikator użytkownika do administratora.</span><span class="sxs-lookup"><span data-stu-id="91708-107">To add, remove, or list keys in the managed HSM, user should grant permissions by adding user ID to Administrator.</span></span>

## <span data-ttu-id="91708-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="91708-108">EXAMPLES</span></span>

### <span data-ttu-id="91708-109">Przykład 1. Tworzenie zarządzanego modułu HSM StandardB1</span><span class="sxs-lookup"><span data-stu-id="91708-109">Example 1: Create a StandardB1 managed HSM</span></span>
```powershell
PS C:\> New-AzManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="91708-110">To polecenie tworzy zarządzany HSM o nazwie myhsm w lokalizacji eastus2euap.</span><span class="sxs-lookup"><span data-stu-id="91708-110">This command creates a managed HSM named myhsm in the location eastus2euap.</span></span> <span data-ttu-id="91708-111">Polecenie dodaje zarządzany składnik HSM do grupy zasobów o nazwie myrg1.</span><span class="sxs-lookup"><span data-stu-id="91708-111">The command adds the managed HSM to the resource group named myrg1.</span></span> <span data-ttu-id="91708-112">Ponieważ polecenie nie określa wartości parametru *SKU* , tworzy Standard_B1 zarządzanym HSM.</span><span class="sxs-lookup"><span data-stu-id="91708-112">Because the command does not specify a value for the *SKU* parameter, it creates a Standard_B1 managed HSM.</span></span>

### <span data-ttu-id="91708-113">Przykład 2: Tworzenie zarządzanego modułu HSM CustomB32</span><span class="sxs-lookup"><span data-stu-id="91708-113">Example 2: Create a CustomB32 managed HSM</span></span>
```powershell
PS C:\>New-AzManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" -Sku 'CustomB32'
Name  Resource Group Name Location    SKU

----  ------------------- --------    ---
myhsm myrg1               eastus2euap CustomB32
```

                      

<span data-ttu-id="91708-114">To polecenie tworzy zarządzany HSM, podobnie jak w poprzednim przykładzie.</span><span class="sxs-lookup"><span data-stu-id="91708-114">This command creates a managed HSM, just like the previous example.</span></span> <span data-ttu-id="91708-115">Jednak określa wartość CustomB32 dla parametru *SKU* w celu utworzenia CustomB32 zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="91708-115">However, it specifies a value of CustomB32 for the *SKU* parameter to create a CustomB32 managed HSM.</span></span>

## <span data-ttu-id="91708-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="91708-116">PARAMETERS</span></span>

### <span data-ttu-id="91708-117">-Administrator</span><span class="sxs-lookup"><span data-stu-id="91708-117">-Administrator</span></span>
<span data-ttu-id="91708-118">Początkowy identyfikator obiektu administratora dla tej puli zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="91708-118">Initial administrator object id for this managed HSM pool.</span></span>

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

### <span data-ttu-id="91708-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91708-119">-AsJob</span></span>
<span data-ttu-id="91708-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="91708-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91708-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91708-121">-DefaultProfile</span></span>
<span data-ttu-id="91708-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="91708-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91708-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="91708-123">-Location</span></span>
<span data-ttu-id="91708-124">Określa obszar Azure, w którym ma zostać utworzony magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="91708-124">Specifies the Azure region in which to create the key vault.</span></span>
<span data-ttu-id="91708-125">Użyj polecenia Get-AzResourceProvider z parametrem ProviderNamespace, aby wyświetlić wybrane opcje.</span><span class="sxs-lookup"><span data-stu-id="91708-125">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

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

### <span data-ttu-id="91708-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="91708-126">-Name</span></span>
<span data-ttu-id="91708-127">Określa nazwę zarządzanego modułu HSM, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="91708-127">Specifies a name of the managed HSM to create.</span></span>
<span data-ttu-id="91708-128">Nazwa może być dowolną kombinacją liter, cyfr lub łączników.</span><span class="sxs-lookup"><span data-stu-id="91708-128">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="91708-129">Nazwa musi zaczynać się i kończyć literą lub cyfrą.</span><span class="sxs-lookup"><span data-stu-id="91708-129">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="91708-130">Nazwa musi być uniwersalnie unikatowa.</span><span class="sxs-lookup"><span data-stu-id="91708-130">The name must be universally unique.</span></span>

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

### <span data-ttu-id="91708-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91708-131">-ResourceGroupName</span></span>
<span data-ttu-id="91708-132">Określa nazwę istniejącej grupy zasobów, w której ma zostać utworzony magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="91708-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="91708-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="91708-133">-Sku</span></span>
<span data-ttu-id="91708-134">Określa jednostkę SKU zarządzanego wystąpienia modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="91708-134">Specifies the SKU of the managed HSM instance.</span></span>

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

### <span data-ttu-id="91708-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="91708-135">-Tag</span></span>
<span data-ttu-id="91708-136">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="91708-136">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="91708-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="91708-137">-Confirm</span></span>
<span data-ttu-id="91708-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91708-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91708-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91708-139">-WhatIf</span></span>
<span data-ttu-id="91708-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91708-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91708-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="91708-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91708-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91708-142">CommonParameters</span></span>
<span data-ttu-id="91708-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91708-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91708-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91708-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91708-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91708-145">INPUTS</span></span>

### <span data-ttu-id="91708-146">System. String</span><span class="sxs-lookup"><span data-stu-id="91708-146">System.String</span></span>

### <span data-ttu-id="91708-147">System. String []</span><span class="sxs-lookup"><span data-stu-id="91708-147">System.String[]</span></span>

### <span data-ttu-id="91708-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="91708-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="91708-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="91708-149">OUTPUTS</span></span>

### <span data-ttu-id="91708-150">Microsoft. Azure. Commands. platforming. models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="91708-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="91708-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="91708-151">NOTES</span></span>

## <span data-ttu-id="91708-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91708-152">RELATED LINKS</span></span>

[<span data-ttu-id="91708-153">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="91708-153">Get-AzManagedHsm</span></span>](./Get-AzManagedHsm.md)

[<span data-ttu-id="91708-154">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="91708-154">Remove-AzManagedHsm</span></span>](./Remove-AzManagedHsm.md)

[<span data-ttu-id="91708-155">Update-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="91708-155">Update-AzManagedHsm</span></span>](./Update-AzManagedHsm.md)