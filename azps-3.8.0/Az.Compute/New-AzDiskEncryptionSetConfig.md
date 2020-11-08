---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionsetconfig.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
ms.openlocfilehash: 5d38a1104d1f2d1f569560027c540a2c8605bdae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050433"
---
# <span data-ttu-id="ae154-101">New-AzDiskEncryptionSetConfig</span><span class="sxs-lookup"><span data-stu-id="ae154-101">New-AzDiskEncryptionSetConfig</span></span>

## <span data-ttu-id="ae154-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae154-102">SYNOPSIS</span></span>
<span data-ttu-id="ae154-103">Umożliwia utworzenie obiektu zestawu konfigurowalnego szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="ae154-103">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="ae154-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae154-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSetConfig [-Location] <String> [[-Tag] <Hashtable>] [[-IdentityType] <String>]
 [[-SourceVaultId] <String>] [-KeyUrl <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae154-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ae154-105">DESCRIPTION</span></span>
<span data-ttu-id="ae154-106">Umożliwia utworzenie obiektu zestawu konfigurowalnego szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="ae154-106">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="ae154-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae154-107">EXAMPLES</span></span>

### <span data-ttu-id="ae154-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ae154-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="ae154-109">Umożliwia utworzenie zestawu do szyfrowania dysków za pomocą danego klucza aktywnego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="ae154-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="ae154-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae154-110">PARAMETERS</span></span>

### <span data-ttu-id="ae154-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae154-111">-DefaultProfile</span></span>
<span data-ttu-id="ae154-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae154-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae154-113">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="ae154-113">-IdentityType</span></span>
<span data-ttu-id="ae154-114">Typ tożsamości zarządzanej używanej przez DiskEncryptionSet.</span><span class="sxs-lookup"><span data-stu-id="ae154-114">The type of Managed Identity used by the DiskEncryptionSet.</span></span> <span data-ttu-id="ae154-115">Obsługiwane są tylko SystemAssigned.</span><span class="sxs-lookup"><span data-stu-id="ae154-115">Only SystemAssigned is supported.</span></span>

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

### <span data-ttu-id="ae154-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="ae154-116">-KeyUrl</span></span>
<span data-ttu-id="ae154-117">Adres URL wskazujący aktywny klucz w magazynie kluczy</span><span class="sxs-lookup"><span data-stu-id="ae154-117">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="ae154-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ae154-118">-Location</span></span>
<span data-ttu-id="ae154-119">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="ae154-119">Specifies a location.</span></span>

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

### <span data-ttu-id="ae154-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="ae154-120">-SourceVaultId</span></span>
<span data-ttu-id="ae154-121">Identyfikator zasobu w magazynie kluczy zawierającym aktywny klucz.</span><span class="sxs-lookup"><span data-stu-id="ae154-121">Resource id of the KeyVault containing the active key.</span></span>

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

### <span data-ttu-id="ae154-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="ae154-122">-Tag</span></span>
<span data-ttu-id="ae154-123">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ae154-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ae154-124">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="ae154-124">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ae154-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ae154-125">-Confirm</span></span>
<span data-ttu-id="ae154-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae154-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae154-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae154-127">-WhatIf</span></span>
<span data-ttu-id="ae154-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae154-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae154-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ae154-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae154-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae154-130">CommonParameters</span></span>
<span data-ttu-id="ae154-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae154-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae154-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae154-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae154-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae154-133">INPUTS</span></span>

### <span data-ttu-id="ae154-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ae154-134">System.String</span></span>

### <span data-ttu-id="ae154-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ae154-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ae154-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae154-136">OUTPUTS</span></span>

### <span data-ttu-id="ae154-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="ae154-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="ae154-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae154-138">NOTES</span></span>

## <span data-ttu-id="ae154-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae154-139">RELATED LINKS</span></span>
