---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azdiskencryptionsetconfig.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
ms.openlocfilehash: 358481a4c8ba20e8c8aa6f2ed47ebaa13225b939
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957601"
---
# <span data-ttu-id="bb824-101">New-AzDiskEncryptionSetConfig</span><span class="sxs-lookup"><span data-stu-id="bb824-101">New-AzDiskEncryptionSetConfig</span></span>

## <span data-ttu-id="bb824-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb824-102">SYNOPSIS</span></span>
<span data-ttu-id="bb824-103">Tworzy konfigurowalny obiekt zestawu szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="bb824-103">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="bb824-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bb824-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSetConfig [-Location] <String> [[-Tag] <Hashtable>] [[-IdentityType] <String>]
 [[-SourceVaultId] <String>] [-KeyUrl <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb824-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bb824-105">DESCRIPTION</span></span>
<span data-ttu-id="bb824-106">Tworzy konfigurowalny obiekt zestawu szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="bb824-106">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="bb824-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bb824-107">EXAMPLES</span></span>

### <span data-ttu-id="bb824-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bb824-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="bb824-109">Tworzy zestaw szyfrowania dysku przy użyciu danego aktywnego klucza w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="bb824-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="bb824-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb824-110">PARAMETERS</span></span>

### <span data-ttu-id="bb824-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb824-111">-DefaultProfile</span></span>
<span data-ttu-id="bb824-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb824-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb824-113">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="bb824-113">-EncryptionType</span></span>
<span data-ttu-id="bb824-114">Skorzystaj z tej funkcji, aby ustawić typ szyfrowania zestawu szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="bb824-114">Use this to set the encryption type of the disk encryption set.</span></span> <span data-ttu-id="bb824-115">Dostępne wartości to: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey".</span><span class="sxs-lookup"><span data-stu-id="bb824-115">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'.</span></span>

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

### <span data-ttu-id="bb824-116">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="bb824-116">-IdentityType</span></span>
<span data-ttu-id="bb824-117">Typ tożsamości zarządzanej używany przez zestaw DiskEncryptionSet.</span><span class="sxs-lookup"><span data-stu-id="bb824-117">The type of Managed Identity used by the DiskEncryptionSet.</span></span> <span data-ttu-id="bb824-118">Obsługiwany jest tylko systemAssigned.</span><span class="sxs-lookup"><span data-stu-id="bb824-118">Only SystemAssigned is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb824-119">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="bb824-119">-KeyUrl</span></span>
<span data-ttu-id="bb824-120">Adres URL, który wskaże aktywny klucz w aplikacji KeyVault</span><span class="sxs-lookup"><span data-stu-id="bb824-120">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="bb824-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bb824-121">-Location</span></span>
<span data-ttu-id="bb824-122">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="bb824-122">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb824-123">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="bb824-123">-SourceVaultId</span></span>
<span data-ttu-id="bb824-124">Identyfikator zasobu usługi KeyVault zawierający klucz aktywny.</span><span class="sxs-lookup"><span data-stu-id="bb824-124">Resource id of the KeyVault containing the active key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb824-125">— Tag</span><span class="sxs-lookup"><span data-stu-id="bb824-125">-Tag</span></span>
<span data-ttu-id="bb824-126">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="bb824-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bb824-127">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="bb824-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="bb824-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bb824-128">-Confirm</span></span>
<span data-ttu-id="bb824-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bb824-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb824-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb824-130">-WhatIf</span></span>
<span data-ttu-id="bb824-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb824-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb824-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bb824-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb824-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb824-133">CommonParameters</span></span>
<span data-ttu-id="bb824-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb824-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb824-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb824-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb824-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb824-136">INPUTS</span></span>

### <span data-ttu-id="bb824-137">System.String</span><span class="sxs-lookup"><span data-stu-id="bb824-137">System.String</span></span>

### <span data-ttu-id="bb824-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="bb824-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bb824-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb824-139">OUTPUTS</span></span>

### <span data-ttu-id="bb824-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="bb824-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="bb824-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bb824-141">NOTES</span></span>

## <span data-ttu-id="bb824-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb824-142">RELATED LINKS</span></span>
