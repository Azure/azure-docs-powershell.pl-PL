---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
ms.openlocfilehash: 0e95179dcd2b1948b55526f3f2a8bfd5bb1a8834
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177403"
---
# <span data-ttu-id="7e23f-101">Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="7e23f-101">Update-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="7e23f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e23f-102">SYNOPSIS</span></span>
<span data-ttu-id="7e23f-103">Aktualizuje zestaw szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="7e23f-103">Updates a disk encryption set.</span></span>

## <span data-ttu-id="7e23f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7e23f-104">SYNTAX</span></span>

### <span data-ttu-id="7e23f-105">DefaultParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="7e23f-105">DefaultParameter (Default)</span></span>
```
Update-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-KeyUrl <String>]
 [-SourceVaultId <String>] [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e23f-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="7e23f-106">ResourceIdParameter</span></span>
```
Update-AzDiskEncryptionSet [-ResourceId] <String> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e23f-107">ObjectParameters</span><span class="sxs-lookup"><span data-stu-id="7e23f-107">ObjectParameter</span></span>
```
Update-AzDiskEncryptionSet [-InputObject] <PSDiskEncryptionSet> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e23f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7e23f-108">DESCRIPTION</span></span>
<span data-ttu-id="7e23f-109">Aktualizuje zestaw szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="7e23f-109">Updates a disk encryption set.</span></span>

## <span data-ttu-id="7e23f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7e23f-110">EXAMPLES</span></span>

### <span data-ttu-id="7e23f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7e23f-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1;
```

<span data-ttu-id="7e23f-112">Aktualizuje zestaw szyfrowania dysku przy użyciu danego aktywnego klucza w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="7e23f-112">Updates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="7e23f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e23f-113">PARAMETERS</span></span>

### <span data-ttu-id="7e23f-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7e23f-114">-AsJob</span></span>
<span data-ttu-id="7e23f-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7e23f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e23f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e23f-116">-DefaultProfile</span></span>
<span data-ttu-id="7e23f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7e23f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e23f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e23f-118">-InputObject</span></span>
<span data-ttu-id="7e23f-119">Obiekt lokalny zestawu szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="7e23f-119">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: ObjectParameter
Aliases: DiskEncryptionSet

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e23f-120">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="7e23f-120">-KeyUrl</span></span>
<span data-ttu-id="7e23f-121">Adres URL, który wskaże aktywny klucz w aplikacji KeyVault</span><span class="sxs-lookup"><span data-stu-id="7e23f-121">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="7e23f-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7e23f-122">-Name</span></span>
<span data-ttu-id="7e23f-123">Nazwa zestawu szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="7e23f-123">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e23f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e23f-124">-ResourceGroupName</span></span>
<span data-ttu-id="7e23f-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7e23f-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e23f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e23f-126">-ResourceId</span></span>
<span data-ttu-id="7e23f-127">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="7e23f-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e23f-128">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="7e23f-128">-SourceVaultId</span></span>
<span data-ttu-id="7e23f-129">Identyfikator zasobu usługi KeyVault zawierający klucz aktywny.</span><span class="sxs-lookup"><span data-stu-id="7e23f-129">Resource id of the KeyVault containing the active key.</span></span>

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

### <span data-ttu-id="7e23f-130">— Tag</span><span class="sxs-lookup"><span data-stu-id="7e23f-130">-Tag</span></span>
<span data-ttu-id="7e23f-131">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="7e23f-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7e23f-132">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="7e23f-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e23f-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7e23f-133">-Confirm</span></span>
<span data-ttu-id="7e23f-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7e23f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e23f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e23f-135">-WhatIf</span></span>
<span data-ttu-id="7e23f-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e23f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e23f-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7e23f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e23f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e23f-138">CommonParameters</span></span>
<span data-ttu-id="7e23f-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e23f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e23f-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e23f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e23f-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e23f-141">INPUTS</span></span>

### <span data-ttu-id="7e23f-142">System.String</span><span class="sxs-lookup"><span data-stu-id="7e23f-142">System.String</span></span>

### <span data-ttu-id="7e23f-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="7e23f-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

### <span data-ttu-id="7e23f-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7e23f-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7e23f-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e23f-145">OUTPUTS</span></span>

### <span data-ttu-id="7e23f-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="7e23f-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="7e23f-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7e23f-147">NOTES</span></span>

## <span data-ttu-id="7e23f-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e23f-148">RELATED LINKS</span></span>
