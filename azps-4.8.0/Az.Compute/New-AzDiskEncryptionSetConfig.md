---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionsetconfig.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
ms.openlocfilehash: bfcb306b12c047c9207e0ef2f1d82bf6eaffc4d3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063610"
---
# <span data-ttu-id="4ee65-101">New-AzDiskEncryptionSetConfig</span><span class="sxs-lookup"><span data-stu-id="4ee65-101">New-AzDiskEncryptionSetConfig</span></span>

## <span data-ttu-id="4ee65-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4ee65-102">SYNOPSIS</span></span>
<span data-ttu-id="4ee65-103">Umożliwia utworzenie obiektu zestawu konfigurowalnego szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="4ee65-103">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="4ee65-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4ee65-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSetConfig [-Location] <String> [[-Tag] <Hashtable>] [[-IdentityType] <String>]
 [[-SourceVaultId] <String>] [-KeyUrl <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ee65-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4ee65-105">DESCRIPTION</span></span>
<span data-ttu-id="4ee65-106">Umożliwia utworzenie obiektu zestawu konfigurowalnego szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="4ee65-106">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="4ee65-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4ee65-107">EXAMPLES</span></span>

### <span data-ttu-id="4ee65-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4ee65-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="4ee65-109">Umożliwia utworzenie zestawu do szyfrowania dysków za pomocą danego klucza aktywnego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="4ee65-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="4ee65-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ee65-110">PARAMETERS</span></span>

### <span data-ttu-id="4ee65-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ee65-111">-DefaultProfile</span></span>
<span data-ttu-id="4ee65-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ee65-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ee65-113">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="4ee65-113">-EncryptionType</span></span>
<span data-ttu-id="4ee65-114">Użyj tej funkcji, aby ustawić typ szyfrowania zestawu do szyfrowania dysków.</span><span class="sxs-lookup"><span data-stu-id="4ee65-114">Use this to set the encryption type of the disk encryption set.</span></span> <span data-ttu-id="4ee65-115">Dostępne wartości: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey".</span><span class="sxs-lookup"><span data-stu-id="4ee65-115">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'.</span></span>

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

### <span data-ttu-id="4ee65-116">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="4ee65-116">-IdentityType</span></span>
<span data-ttu-id="4ee65-117">Typ tożsamości zarządzanej używanej przez DiskEncryptionSet.</span><span class="sxs-lookup"><span data-stu-id="4ee65-117">The type of Managed Identity used by the DiskEncryptionSet.</span></span> <span data-ttu-id="4ee65-118">Obsługiwane są tylko SystemAssigned.</span><span class="sxs-lookup"><span data-stu-id="4ee65-118">Only SystemAssigned is supported.</span></span>

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

### <span data-ttu-id="4ee65-119">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="4ee65-119">-KeyUrl</span></span>
<span data-ttu-id="4ee65-120">Adres URL wskazujący aktywny klucz w magazynie kluczy</span><span class="sxs-lookup"><span data-stu-id="4ee65-120">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="4ee65-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4ee65-121">-Location</span></span>
<span data-ttu-id="4ee65-122">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="4ee65-122">Specifies a location.</span></span>

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

### <span data-ttu-id="4ee65-123">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="4ee65-123">-SourceVaultId</span></span>
<span data-ttu-id="4ee65-124">Identyfikator zasobu w magazynie kluczy zawierającym aktywny klucz.</span><span class="sxs-lookup"><span data-stu-id="4ee65-124">Resource id of the KeyVault containing the active key.</span></span>

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

### <span data-ttu-id="4ee65-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="4ee65-125">-Tag</span></span>
<span data-ttu-id="4ee65-126">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="4ee65-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4ee65-127">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="4ee65-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4ee65-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4ee65-128">-Confirm</span></span>
<span data-ttu-id="4ee65-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ee65-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ee65-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ee65-130">-WhatIf</span></span>
<span data-ttu-id="4ee65-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ee65-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ee65-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4ee65-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ee65-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ee65-133">CommonParameters</span></span>
<span data-ttu-id="4ee65-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ee65-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ee65-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ee65-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ee65-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ee65-136">INPUTS</span></span>

### <span data-ttu-id="4ee65-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4ee65-137">System.String</span></span>

### <span data-ttu-id="4ee65-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4ee65-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4ee65-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4ee65-139">OUTPUTS</span></span>

### <span data-ttu-id="4ee65-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="4ee65-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="4ee65-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4ee65-141">NOTES</span></span>

## <span data-ttu-id="4ee65-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ee65-142">RELATED LINKS</span></span>
