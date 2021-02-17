---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: f96aa323486144ec9d4dcb04ff00f408a763a81a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243371"
---
# <span data-ttu-id="1be27-101">Import-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="1be27-101">Import-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="1be27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1be27-102">SYNOPSIS</span></span>
<span data-ttu-id="1be27-103">Wcześniej wyeksportowano dane z domeny zabezpieczeń do zarządzanego systemu HSM.</span><span class="sxs-lookup"><span data-stu-id="1be27-103">Imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="1be27-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1be27-104">SYNTAX</span></span>

### <span data-ttu-id="1be27-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="1be27-105">ByName (Default)</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1be27-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1be27-106">ByInputObject</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru]
 -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1be27-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1be27-107">DESCRIPTION</span></span>
<span data-ttu-id="1be27-108">To polecenie cmdlet importuje poprzednio wyeksportowane dane z domeny zabezpieczeń do zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="1be27-108">This cmdlet imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="1be27-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1be27-109">EXAMPLES</span></span>

### <span data-ttu-id="1be27-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1be27-110">Example 1</span></span>
```powershell
PS C:\> $keys = @{PublicKey = "sd1.cer"; PrivateKey = "sd1.key"}, @{PublicKey = "sd2.cer"; PrivateKey = "sd2.key"}, @{PublicKey = "sd3.cer"; PrivateKey = "sd3.key"}
PS C:\> Import-AzKeyVaultSecurityDomain -Name testmhsm -Keys $keys -SecurityDomainPath {pathOfBackup}\sd.ps.json
```

<span data-ttu-id="1be27-111">Najpierw należy zapewnić klucze do odszyfrowania danych domeny zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="1be27-111">First, the keys need be provided to decrypt the security domain data.</span></span>
<span data-ttu-id="1be27-112">Następnie polecenie **Import-AzKeyVaultSecurityDomain** przywraca poprzednią kopię zapasową danych domeny zabezpieczeń do zarządzanego hsm przy użyciu tych kluczy.</span><span class="sxs-lookup"><span data-stu-id="1be27-112">Then, The **Import-AzKeyVaultSecurityDomain** command restores previous backed up security domain data to a managed HSM using these keys.</span></span>

## <span data-ttu-id="1be27-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1be27-113">PARAMETERS</span></span>

### <span data-ttu-id="1be27-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1be27-114">-DefaultProfile</span></span>
<span data-ttu-id="1be27-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1be27-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1be27-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1be27-116">-InputObject</span></span>
<span data-ttu-id="1be27-117">Obiekt reprezentujący zarządzany moduł HSM.</span><span class="sxs-lookup"><span data-stu-id="1be27-117">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="1be27-118">— Klawisze</span><span class="sxs-lookup"><span data-stu-id="1be27-118">-Keys</span></span>
<span data-ttu-id="1be27-119">Informacje o kluczach używanych do odszyfrowywania danych domeny zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="1be27-119">Information about the keys that are used to decrypt the security domain data.</span></span>
<span data-ttu-id="1be27-120">Zobacz przykłady sposobu skonstruowania.</span><span class="sxs-lookup"><span data-stu-id="1be27-120">See examples for how it is constructed.</span></span>

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

### <span data-ttu-id="1be27-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1be27-121">-Name</span></span>
<span data-ttu-id="1be27-122">Nazwa zarządzanego hsm.</span><span class="sxs-lookup"><span data-stu-id="1be27-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="1be27-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1be27-123">-PassThru</span></span>
<span data-ttu-id="1be27-124">Jeśli to zwrócę, wartość logiczna zostanie zwrócona, gdy polecenie cmdlet zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="1be27-124">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="1be27-125">- SecurityDomainPath</span><span class="sxs-lookup"><span data-stu-id="1be27-125">-SecurityDomainPath</span></span>
<span data-ttu-id="1be27-126">Określ ścieżkę do zaszyfrowanych danych domeny zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="1be27-126">Specify the path to the encrypted security domain data.</span></span>

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

### <span data-ttu-id="1be27-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1be27-127">-Confirm</span></span>
<span data-ttu-id="1be27-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1be27-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1be27-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1be27-129">-WhatIf</span></span>
<span data-ttu-id="1be27-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1be27-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1be27-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1be27-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1be27-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1be27-132">CommonParameters</span></span>
<span data-ttu-id="1be27-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1be27-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1be27-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1be27-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1be27-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1be27-135">INPUTS</span></span>

### <span data-ttu-id="1be27-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1be27-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="1be27-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1be27-137">OUTPUTS</span></span>

### <span data-ttu-id="1be27-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1be27-138">System.Boolean</span></span>

## <span data-ttu-id="1be27-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1be27-139">NOTES</span></span>

## <span data-ttu-id="1be27-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1be27-140">RELATED LINKS</span></span>
