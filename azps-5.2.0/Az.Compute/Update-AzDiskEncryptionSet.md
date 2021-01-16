---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
ms.openlocfilehash: 0e95179dcd2b1948b55526f3f2a8bfd5bb1a8834
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335533"
---
# <span data-ttu-id="67212-101">Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="67212-101">Update-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="67212-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="67212-102">SYNOPSIS</span></span>
<span data-ttu-id="67212-103">Aktualizuje zestaw szyfrowania dysków.</span><span class="sxs-lookup"><span data-stu-id="67212-103">Updates a disk encryption set.</span></span>

## <span data-ttu-id="67212-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="67212-104">SYNTAX</span></span>

### <span data-ttu-id="67212-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="67212-105">DefaultParameter (Default)</span></span>
```
Update-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-KeyUrl <String>]
 [-SourceVaultId <String>] [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67212-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="67212-106">ResourceIdParameter</span></span>
```
Update-AzDiskEncryptionSet [-ResourceId] <String> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67212-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="67212-107">ObjectParameter</span></span>
```
Update-AzDiskEncryptionSet [-InputObject] <PSDiskEncryptionSet> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="67212-108">Opis</span><span class="sxs-lookup"><span data-stu-id="67212-108">DESCRIPTION</span></span>
<span data-ttu-id="67212-109">Aktualizuje zestaw szyfrowania dysków.</span><span class="sxs-lookup"><span data-stu-id="67212-109">Updates a disk encryption set.</span></span>

## <span data-ttu-id="67212-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="67212-110">EXAMPLES</span></span>

### <span data-ttu-id="67212-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="67212-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1;
```

<span data-ttu-id="67212-112">Aktualizuje zestaw szyfrowanie dysków przy użyciu podanego klucza aktywnego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="67212-112">Updates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="67212-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="67212-113">PARAMETERS</span></span>

### <span data-ttu-id="67212-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67212-114">-AsJob</span></span>
<span data-ttu-id="67212-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="67212-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67212-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67212-116">-DefaultProfile</span></span>
<span data-ttu-id="67212-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="67212-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67212-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="67212-118">-InputObject</span></span>
<span data-ttu-id="67212-119">Lokalny obiekt zestawu do szyfrowania dysków.</span><span class="sxs-lookup"><span data-stu-id="67212-119">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="67212-120">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="67212-120">-KeyUrl</span></span>
<span data-ttu-id="67212-121">Adres URL wskazujący aktywny klucz w magazynie kluczy</span><span class="sxs-lookup"><span data-stu-id="67212-121">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="67212-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="67212-122">-Name</span></span>
<span data-ttu-id="67212-123">Nazwa zestawu szyfrowania dysków.</span><span class="sxs-lookup"><span data-stu-id="67212-123">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="67212-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67212-124">-ResourceGroupName</span></span>
<span data-ttu-id="67212-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="67212-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="67212-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67212-126">-ResourceId</span></span>
<span data-ttu-id="67212-127">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="67212-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="67212-128">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="67212-128">-SourceVaultId</span></span>
<span data-ttu-id="67212-129">Identyfikator zasobu w magazynie kluczy zawierającym aktywny klucz.</span><span class="sxs-lookup"><span data-stu-id="67212-129">Resource id of the KeyVault containing the active key.</span></span>

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

### <span data-ttu-id="67212-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="67212-130">-Tag</span></span>
<span data-ttu-id="67212-131">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="67212-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="67212-132">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="67212-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="67212-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="67212-133">-Confirm</span></span>
<span data-ttu-id="67212-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67212-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67212-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67212-135">-WhatIf</span></span>
<span data-ttu-id="67212-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67212-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67212-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="67212-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67212-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67212-138">CommonParameters</span></span>
<span data-ttu-id="67212-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67212-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67212-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67212-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67212-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67212-141">INPUTS</span></span>

### <span data-ttu-id="67212-142">System. String</span><span class="sxs-lookup"><span data-stu-id="67212-142">System.String</span></span>

### <span data-ttu-id="67212-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="67212-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

### <span data-ttu-id="67212-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="67212-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="67212-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="67212-145">OUTPUTS</span></span>

### <span data-ttu-id="67212-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="67212-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="67212-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="67212-147">NOTES</span></span>

## <span data-ttu-id="67212-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67212-148">RELATED LINKS</span></span>
