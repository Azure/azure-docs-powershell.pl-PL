---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
ms.openlocfilehash: 3e2e04e2e489b9c9322c62d1c7006490d7bf9bd2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957610"
---
# <span data-ttu-id="d2a11-101">New-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="d2a11-101">New-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="d2a11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2a11-102">SYNOPSIS</span></span>
<span data-ttu-id="d2a11-103">Tworzy zestaw szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="d2a11-103">Creates a disk encryption set.</span></span>

## <span data-ttu-id="d2a11-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d2a11-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <PSDiskEncryptionSet>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2a11-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d2a11-105">DESCRIPTION</span></span>
<span data-ttu-id="d2a11-106">Tworzy zestaw szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="d2a11-106">Creates a disk encryption set.</span></span>

## <span data-ttu-id="d2a11-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d2a11-107">EXAMPLES</span></span>

### <span data-ttu-id="d2a11-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d2a11-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="d2a11-109">Tworzy zestaw szyfrowania dysku przy użyciu danego aktywnego klucza w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="d2a11-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="d2a11-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2a11-110">PARAMETERS</span></span>

### <span data-ttu-id="d2a11-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d2a11-111">-AsJob</span></span>
<span data-ttu-id="d2a11-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d2a11-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2a11-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2a11-113">-DefaultProfile</span></span>
<span data-ttu-id="d2a11-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2a11-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2a11-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2a11-115">-InputObject</span></span>
<span data-ttu-id="d2a11-116">Obiekt lokalny zestawu szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="d2a11-116">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="d2a11-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d2a11-117">-Name</span></span>
<span data-ttu-id="d2a11-118">Nazwa zestawu szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="d2a11-118">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="d2a11-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2a11-119">-ResourceGroupName</span></span>
<span data-ttu-id="d2a11-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d2a11-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d2a11-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d2a11-121">-Confirm</span></span>
<span data-ttu-id="d2a11-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d2a11-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2a11-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2a11-123">-WhatIf</span></span>
<span data-ttu-id="d2a11-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2a11-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2a11-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d2a11-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2a11-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2a11-126">CommonParameters</span></span>
<span data-ttu-id="d2a11-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2a11-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2a11-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2a11-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2a11-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2a11-129">INPUTS</span></span>

### <span data-ttu-id="d2a11-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d2a11-130">System.String</span></span>

### <span data-ttu-id="d2a11-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="d2a11-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="d2a11-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2a11-132">OUTPUTS</span></span>

### <span data-ttu-id="d2a11-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="d2a11-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="d2a11-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d2a11-134">NOTES</span></span>

## <span data-ttu-id="d2a11-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2a11-135">RELATED LINKS</span></span>
