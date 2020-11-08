---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsmsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmSecurityDomain.md
ms.openlocfilehash: f743b408917e575005589598a49fafbd8cc95379
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234665"
---
# <span data-ttu-id="cf0ed-101">Restore-AzManagedHsmSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="cf0ed-101">Restore-AzManagedHsmSecurityDomain</span></span>

## <span data-ttu-id="cf0ed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cf0ed-102">SYNOPSIS</span></span>
<span data-ttu-id="cf0ed-103">Przywraca wcześniejsze kopie zapasowe danych domeny zabezpieczeń do zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="cf0ed-103">Restores previous backed up security domain data to a managed HSM.</span></span>

## <span data-ttu-id="cf0ed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cf0ed-104">SYNTAX</span></span>

### <span data-ttu-id="cf0ed-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cf0ed-105">ByName (Default)</span></span>
```
Restore-AzManagedHsmSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf0ed-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cf0ed-106">ByInputObject</span></span>
```
Restore-AzManagedHsmSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru]
 -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf0ed-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cf0ed-107">DESCRIPTION</span></span>
<span data-ttu-id="cf0ed-108">To polecenie cmdlet przywraca wcześniejsze kopie zapasowe danych domeny zabezpieczeń do zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="cf0ed-108">This cmdlet restores previous backed up security domain data to a managed HSM.</span></span>

## <span data-ttu-id="cf0ed-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cf0ed-109">EXAMPLES</span></span>

### <span data-ttu-id="cf0ed-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cf0ed-110">Example 1</span></span>
```powershell
PS C:\> $keys = @{PublicKey = "sd1.cer"; PrivateKey = "sd1.key"}, @{PublicKey = "sd2.cer"; PrivateKey = "sd2.key"}, @{PublicKey = "sd3.cer"; PrivateKey = "sd3.key"}
PS C:\> Restore-AzManagedHsmSecurityDomain -Name testmhsm -Keys $keys -SecurityDomainPath {pathOfBackup}\sd.ps.json
```

<span data-ttu-id="cf0ed-111">Najpierw należy podać klucze, aby odszyfrować dane domeny zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="cf0ed-111">First, the keys need be provided to decrypt the security domain data.</span></span> <span data-ttu-id="cf0ed-112">Następnie polecenie **Restore-AzManagedHsmSecurityDomain** przywraca poprzednie kopie zapasowe danych domeny zabezpieczeń do zarządzanego modułu HSM przy użyciu tych kluczy.</span><span class="sxs-lookup"><span data-stu-id="cf0ed-112">Then, The **Restore-AzManagedHsmSecurityDomain** command restores previous backed up security domain data to a managed HSM using these keys.</span></span>

## <span data-ttu-id="cf0ed-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cf0ed-113">PARAMETERS</span></span>

### <span data-ttu-id="cf0ed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf0ed-114">-DefaultProfile</span></span>
<span data-ttu-id="cf0ed-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cf0ed-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf0ed-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cf0ed-116">-InputObject</span></span>
<span data-ttu-id="cf0ed-117">Obiekt reprezentujący zarządzany element HSM.</span><span class="sxs-lookup"><span data-stu-id="cf0ed-117">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="cf0ed-118">-Keys</span><span class="sxs-lookup"><span data-stu-id="cf0ed-118">-Keys</span></span>
<span data-ttu-id="cf0ed-119">Informacje o kluczach używanych do odszyfrowania danych domeny zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="cf0ed-119">Information about the keys that are used to decrypt the security domain data.</span></span>
<span data-ttu-id="cf0ed-120">Zobacz przykłady ich konstruowania.</span><span class="sxs-lookup"><span data-stu-id="cf0ed-120">See examples for how it is constructed.</span></span>

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

### <span data-ttu-id="cf0ed-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cf0ed-121">-Name</span></span>
<span data-ttu-id="cf0ed-122">Nazwa zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="cf0ed-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="cf0ed-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf0ed-123">-PassThru</span></span>
<span data-ttu-id="cf0ed-124">Po określeniu wartość logiczna zostanie zwrócona, gdy polecenie cmdlet zostanie wykonane pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="cf0ed-124">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="cf0ed-125">-SecurityDomainPath</span><span class="sxs-lookup"><span data-stu-id="cf0ed-125">-SecurityDomainPath</span></span>
<span data-ttu-id="cf0ed-126">Określ ścieżkę do danych zaszyfrowanej domeny zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="cf0ed-126">Specify the path to the encrypted security domain data.</span></span>

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

### <span data-ttu-id="cf0ed-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cf0ed-127">-Confirm</span></span>
<span data-ttu-id="cf0ed-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf0ed-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf0ed-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf0ed-129">-WhatIf</span></span>
<span data-ttu-id="cf0ed-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf0ed-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf0ed-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cf0ed-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf0ed-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf0ed-132">CommonParameters</span></span>
<span data-ttu-id="cf0ed-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf0ed-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf0ed-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf0ed-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf0ed-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf0ed-135">INPUTS</span></span>

### <span data-ttu-id="cf0ed-136">Microsoft. Azure. Commands. platforming. models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="cf0ed-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="cf0ed-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cf0ed-137">OUTPUTS</span></span>

### <span data-ttu-id="cf0ed-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cf0ed-138">System.Boolean</span></span>

## <span data-ttu-id="cf0ed-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cf0ed-139">NOTES</span></span>

## <span data-ttu-id="cf0ed-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf0ed-140">RELATED LINKS</span></span>
