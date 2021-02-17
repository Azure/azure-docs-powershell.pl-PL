---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 061b16758386cf2e279250a1ab72cdcf4180a1f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192363"
---
# <span data-ttu-id="92daa-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="92daa-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="92daa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92daa-102">SYNOPSIS</span></span>
<span data-ttu-id="92daa-103">Usuwa wystawcę certyfikatu z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="92daa-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="92daa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="92daa-104">SYNTAX</span></span>

### <span data-ttu-id="92daa-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="92daa-105">Default (Default)</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92daa-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="92daa-106">InputObject</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92daa-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="92daa-107">DESCRIPTION</span></span>
<span data-ttu-id="92daa-108">Polecenie **cmdlet Remove-AzKeyVaultCertificateIssuer** usuwa wystawcę certyfikatu z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="92daa-108">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="92daa-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="92daa-109">EXAMPLES</span></span>

### <span data-ttu-id="92daa-110">Przykład 1. Usuwanie wystawcy certyfikatu</span><span class="sxs-lookup"><span data-stu-id="92daa-110">Example 1: Remove a certificate issuer</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force

AccountId           :
ApiKey              :
OrganizationDetails :
Name                : TestIssuer01
IssuerProvider      : test
VaultName           : ContosoKV01
```

<span data-ttu-id="92daa-111">To polecenie usuwa wystawcę certyfikatu o nazwie TestIssuer01 z magazynu kluczy ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="92daa-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="92daa-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92daa-112">PARAMETERS</span></span>

### <span data-ttu-id="92daa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92daa-113">-DefaultProfile</span></span>
<span data-ttu-id="92daa-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="92daa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92daa-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="92daa-115">-Force</span></span>
<span data-ttu-id="92daa-116">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="92daa-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="92daa-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92daa-117">-InputObject</span></span>
<span data-ttu-id="92daa-118">Obiekt Wystawca certyfikatu</span><span class="sxs-lookup"><span data-stu-id="92daa-118">Certificate Issuer Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92daa-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="92daa-119">-Name</span></span>
<span data-ttu-id="92daa-120">Określa nazwę wystawcy do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="92daa-120">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92daa-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92daa-121">-PassThru</span></span>
<span data-ttu-id="92daa-122">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="92daa-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="92daa-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="92daa-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="92daa-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="92daa-124">-VaultName</span></span>
<span data-ttu-id="92daa-125">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="92daa-125">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92daa-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="92daa-126">-Confirm</span></span>
<span data-ttu-id="92daa-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="92daa-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92daa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92daa-128">-WhatIf</span></span>
<span data-ttu-id="92daa-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92daa-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92daa-130">Polecenie cmdlet nie zostanie uruchomione. Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92daa-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92daa-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="92daa-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92daa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92daa-132">CommonParameters</span></span>
<span data-ttu-id="92daa-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92daa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92daa-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92daa-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92daa-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92daa-135">INPUTS</span></span>

### <span data-ttu-id="92daa-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="92daa-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="92daa-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="92daa-137">OUTPUTS</span></span>

### <span data-ttu-id="92daa-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="92daa-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="92daa-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="92daa-139">NOTES</span></span>

## <span data-ttu-id="92daa-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92daa-140">RELATED LINKS</span></span>

[<span data-ttu-id="92daa-141">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="92daa-141">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="92daa-142">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="92daa-142">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


