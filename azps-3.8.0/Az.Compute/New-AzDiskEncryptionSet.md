---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
ms.openlocfilehash: 61d8d60925eb1d7e71ca85f92e30516d598facdf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050435"
---
# <span data-ttu-id="7f236-101">New-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="7f236-101">New-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="7f236-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f236-102">SYNOPSIS</span></span>
<span data-ttu-id="7f236-103">Tworzy zestaw szyfrowania dysków.</span><span class="sxs-lookup"><span data-stu-id="7f236-103">Creates a disk encryption set.</span></span>

## <span data-ttu-id="7f236-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f236-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <PSDiskEncryptionSet>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f236-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7f236-105">DESCRIPTION</span></span>
<span data-ttu-id="7f236-106">Tworzy zestaw szyfrowania dysków.</span><span class="sxs-lookup"><span data-stu-id="7f236-106">Creates a disk encryption set.</span></span>

## <span data-ttu-id="7f236-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f236-107">EXAMPLES</span></span>

### <span data-ttu-id="7f236-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7f236-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="7f236-109">Umożliwia utworzenie zestawu do szyfrowania dysków za pomocą danego klucza aktywnego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="7f236-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="7f236-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f236-110">PARAMETERS</span></span>

### <span data-ttu-id="7f236-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f236-111">-AsJob</span></span>
<span data-ttu-id="7f236-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7f236-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7f236-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f236-113">-DefaultProfile</span></span>
<span data-ttu-id="7f236-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f236-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f236-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7f236-115">-InputObject</span></span>
<span data-ttu-id="7f236-116">Lokalny obiekt zestawu do szyfrowania dysków.</span><span class="sxs-lookup"><span data-stu-id="7f236-116">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: (All)
Aliases: DiskEncryptionSet

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f236-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7f236-117">-Name</span></span>
<span data-ttu-id="7f236-118">Nazwa zestawu szyfrowania dysków.</span><span class="sxs-lookup"><span data-stu-id="7f236-118">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f236-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f236-119">-ResourceGroupName</span></span>
<span data-ttu-id="7f236-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7f236-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7f236-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f236-121">-Confirm</span></span>
<span data-ttu-id="7f236-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f236-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f236-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f236-123">-WhatIf</span></span>
<span data-ttu-id="7f236-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f236-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f236-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7f236-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f236-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f236-126">CommonParameters</span></span>
<span data-ttu-id="7f236-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f236-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f236-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f236-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f236-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f236-129">INPUTS</span></span>

### <span data-ttu-id="7f236-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7f236-130">System.String</span></span>

### <span data-ttu-id="7f236-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="7f236-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="7f236-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f236-132">OUTPUTS</span></span>

### <span data-ttu-id="7f236-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="7f236-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="7f236-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f236-134">NOTES</span></span>

## <span data-ttu-id="7f236-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f236-135">RELATED LINKS</span></span>
