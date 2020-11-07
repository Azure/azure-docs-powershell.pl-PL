---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: bca432cb1747ad8333542ec272ef38c2a6c7598f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705136"
---
# <span data-ttu-id="214fc-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="214fc-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="214fc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="214fc-102">SYNOPSIS</span></span>
<span data-ttu-id="214fc-103">Usuwa wystawcę certyfikatu z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="214fc-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="214fc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="214fc-104">SYNTAX</span></span>

### <span data-ttu-id="214fc-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="214fc-105">Default (Default)</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="214fc-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="214fc-106">InputObject</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="214fc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="214fc-107">DESCRIPTION</span></span>
<span data-ttu-id="214fc-108">Polecenie cmdlet **Remove-AzKeyVaultCertificateIssuer** usuwa wystawcę certyfikatu z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="214fc-108">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="214fc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="214fc-109">EXAMPLES</span></span>

### <span data-ttu-id="214fc-110">Przykład 1: usuwanie wystawcy certyfikatu</span><span class="sxs-lookup"><span data-stu-id="214fc-110">Example 1: Remove a certificate issuer</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force

AccountId           :
ApiKey              :
OrganizationDetails :
Name                : TestIssuer01
IssuerProvider      : test
VaultName           : ContosoKV01
```

<span data-ttu-id="214fc-111">To polecenie usuwa wystawcę certyfikatu o nazwie TestIssuer01 z magazynu kluczy ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="214fc-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="214fc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="214fc-112">PARAMETERS</span></span>

### <span data-ttu-id="214fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="214fc-113">-DefaultProfile</span></span>
<span data-ttu-id="214fc-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="214fc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="214fc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="214fc-115">-Force</span></span>
<span data-ttu-id="214fc-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="214fc-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="214fc-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="214fc-117">-InputObject</span></span>
<span data-ttu-id="214fc-118">Obiekt wystawcy certyfikatu</span><span class="sxs-lookup"><span data-stu-id="214fc-118">Certificate Issuer Object</span></span>

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

### <span data-ttu-id="214fc-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="214fc-119">-Name</span></span>
<span data-ttu-id="214fc-120">Określa nazwę wystawcy do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="214fc-120">Specifies the name of the issuer to remove.</span></span>

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

### <span data-ttu-id="214fc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="214fc-121">-PassThru</span></span>
<span data-ttu-id="214fc-122">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="214fc-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="214fc-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="214fc-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="214fc-124">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="214fc-124">-VaultName</span></span>
<span data-ttu-id="214fc-125">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="214fc-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="214fc-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="214fc-126">-Confirm</span></span>
<span data-ttu-id="214fc-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="214fc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="214fc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="214fc-128">-WhatIf</span></span>
<span data-ttu-id="214fc-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="214fc-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="214fc-130">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="214fc-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="214fc-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="214fc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="214fc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="214fc-132">CommonParameters</span></span>
<span data-ttu-id="214fc-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="214fc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="214fc-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="214fc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="214fc-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="214fc-135">INPUTS</span></span>

### <span data-ttu-id="214fc-136">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="214fc-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="214fc-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="214fc-137">OUTPUTS</span></span>

### <span data-ttu-id="214fc-138">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="214fc-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="214fc-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="214fc-139">NOTES</span></span>

## <span data-ttu-id="214fc-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="214fc-140">RELATED LINKS</span></span>

[<span data-ttu-id="214fc-141">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="214fc-141">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="214fc-142">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="214fc-142">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)

