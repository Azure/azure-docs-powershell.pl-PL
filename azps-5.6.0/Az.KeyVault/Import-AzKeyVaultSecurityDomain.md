---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/import-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: 3175685478afada44e8870e772a56ce91992bbc5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001402"
---
# <span data-ttu-id="7dc1a-101">Import-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="7dc1a-101">Import-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="7dc1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7dc1a-102">SYNOPSIS</span></span>
<span data-ttu-id="7dc1a-103">Wcześniej wyeksportowano dane z domeny zabezpieczeń do zarządzanego systemu HSM.</span><span class="sxs-lookup"><span data-stu-id="7dc1a-103">Imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="7dc1a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7dc1a-104">SYNTAX</span></span>

### <span data-ttu-id="7dc1a-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="7dc1a-105">ByName (Default)</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dc1a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7dc1a-106">ByInputObject</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru]
 -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7dc1a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="7dc1a-107">DESCRIPTION</span></span>
<span data-ttu-id="7dc1a-108">To polecenie cmdlet importuje poprzednio wyeksportowane dane z domeny zabezpieczeń do zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="7dc1a-108">This cmdlet imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="7dc1a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7dc1a-109">EXAMPLES</span></span>

### <span data-ttu-id="7dc1a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7dc1a-110">Example 1</span></span>
```powershell
PS C:\> $keys = @{PublicKey = "sd1.cer"; PrivateKey = "sd1.key"}, @{PublicKey = "sd2.cer"; PrivateKey = "sd2.key"}, @{PublicKey = "sd3.cer"; PrivateKey = "sd3.key"}
PS C:\> Import-AzKeyVaultSecurityDomain -Name testmhsm -Keys $keys -SecurityDomainPath {pathOfBackup}\sd.ps.json
```

<span data-ttu-id="7dc1a-111">Najpierw należy zapewnić klucze do odszyfrowania danych domeny zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="7dc1a-111">First, the keys need be provided to decrypt the security domain data.</span></span>
<span data-ttu-id="7dc1a-112">Następnie polecenie **Import-AzKeyVaultSecurityDomain** przywraca poprzednią kopię zapasową danych domeny zabezpieczeń do zarządzanego hsm przy użyciu tych kluczy.</span><span class="sxs-lookup"><span data-stu-id="7dc1a-112">Then, The **Import-AzKeyVaultSecurityDomain** command restores previous backed up security domain data to a managed HSM using these keys.</span></span>

## <span data-ttu-id="7dc1a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7dc1a-113">PARAMETERS</span></span>

### <span data-ttu-id="7dc1a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dc1a-114">-DefaultProfile</span></span>
<span data-ttu-id="7dc1a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7dc1a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7dc1a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7dc1a-116">-InputObject</span></span>
<span data-ttu-id="7dc1a-117">Obiekt reprezentujący zarządzany moduł HSM.</span><span class="sxs-lookup"><span data-stu-id="7dc1a-117">Object representing a managed HSM.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7dc1a-118">— Klawisze</span><span class="sxs-lookup"><span data-stu-id="7dc1a-118">-Keys</span></span>
<span data-ttu-id="7dc1a-119">Informacje o kluczach używanych do odszyfrowywania danych domeny zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="7dc1a-119">Information about the keys that are used to decrypt the security domain data.</span></span>
<span data-ttu-id="7dc1a-120">Zobacz przykłady sposobu ich skonstruowania.</span><span class="sxs-lookup"><span data-stu-id="7dc1a-120">See examples for how it is constructed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.SecurityDomain.Models.KeyPath[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dc1a-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7dc1a-121">-Name</span></span>
<span data-ttu-id="7dc1a-122">Nazwa zarządzanego hsm.</span><span class="sxs-lookup"><span data-stu-id="7dc1a-122">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dc1a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7dc1a-123">-PassThru</span></span>
<span data-ttu-id="7dc1a-124">Jeśli to zwrócę, wartość logiczna zostanie zwrócona, gdy polecenie cmdlet zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="7dc1a-124">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="7dc1a-125">- SecurityDomainPath</span><span class="sxs-lookup"><span data-stu-id="7dc1a-125">-SecurityDomainPath</span></span>
<span data-ttu-id="7dc1a-126">Określ ścieżkę do zaszyfrowanych danych domeny zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="7dc1a-126">Specify the path to the encrypted security domain data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dc1a-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7dc1a-127">-Confirm</span></span>
<span data-ttu-id="7dc1a-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7dc1a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dc1a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dc1a-129">-WhatIf</span></span>
<span data-ttu-id="7dc1a-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dc1a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7dc1a-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7dc1a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dc1a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dc1a-132">CommonParameters</span></span>
<span data-ttu-id="7dc1a-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dc1a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dc1a-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7dc1a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dc1a-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7dc1a-135">INPUTS</span></span>

### <span data-ttu-id="7dc1a-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7dc1a-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="7dc1a-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7dc1a-137">OUTPUTS</span></span>

### <span data-ttu-id="7dc1a-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7dc1a-138">System.Boolean</span></span>

## <span data-ttu-id="7dc1a-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7dc1a-139">NOTES</span></span>

## <span data-ttu-id="7dc1a-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7dc1a-140">RELATED LINKS</span></span>
