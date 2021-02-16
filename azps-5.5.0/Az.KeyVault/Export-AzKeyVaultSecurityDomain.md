---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/export-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: 94f27b497450201715b423babbd55811f2382dd2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203812"
---
# <span data-ttu-id="ab23f-101">Export-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="ab23f-101">Export-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="ab23f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab23f-102">SYNOPSIS</span></span>
<span data-ttu-id="ab23f-103">Eksportuje dane domeny zabezpieczeń zarządzanego hsm.</span><span class="sxs-lookup"><span data-stu-id="ab23f-103">Exports the security domain data of a managed HSM.</span></span>

## <span data-ttu-id="ab23f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ab23f-104">SYNTAX</span></span>

### <span data-ttu-id="ab23f-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="ab23f-105">ByName (Default)</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab23f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ab23f-106">ByInputObject</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab23f-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ab23f-107">DESCRIPTION</span></span>
<span data-ttu-id="ab23f-108">Eksportuje dane domeny zabezpieczeń zarządzanego modułu HSM do zaimportowania do innego HSM.</span><span class="sxs-lookup"><span data-stu-id="ab23f-108">Exports the security domain data of a managed HSM for importing on another HSM.</span></span>

## <span data-ttu-id="ab23f-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ab23f-109">EXAMPLES</span></span>

### <span data-ttu-id="ab23f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ab23f-110">Example 1</span></span>
```powershell
PS C:\Users\username\> Export-AzKeyVaultSecurityDomain -Name testmhsm -Certificates {pathOfCertificates}/sd1.cer, {pathOfCertificates}/sd2.cer, {pathOfCertificates}/sd3.cer -OutputPath {pathOfOutput}/sd.ps.json -Quorum 2
```

<span data-ttu-id="ab23f-111">To polecenie pobiera zarządzany moduł HSM o nazwie testmhsm i zapisuje kopię zapasową tej zarządzanej domeny zabezpieczeń HSM w określonym pliku wyjściowym.</span><span class="sxs-lookup"><span data-stu-id="ab23f-111">This command retrieves the managed HSM named testmhsm and saves a backup of that managed HSM security domain to the specified output file.</span></span>

## <span data-ttu-id="ab23f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab23f-112">PARAMETERS</span></span>

### <span data-ttu-id="ab23f-113">— certyfikaty</span><span class="sxs-lookup"><span data-stu-id="ab23f-113">-Certificates</span></span>
<span data-ttu-id="ab23f-114">Ścieżki do certyfikatów używanych do szyfrowania danych domeny zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="ab23f-114">Paths to the certificates that are used to encrypt the security domain data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab23f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab23f-115">-DefaultProfile</span></span>
<span data-ttu-id="ab23f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab23f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab23f-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="ab23f-117">-Force</span></span>
<span data-ttu-id="ab23f-118">Określ, czy chcesz zastąpić istniejący plik.</span><span class="sxs-lookup"><span data-stu-id="ab23f-118">Specify whether to overwrite existing file.</span></span>

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

### <span data-ttu-id="ab23f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab23f-119">-InputObject</span></span>
<span data-ttu-id="ab23f-120">Obiekt reprezentujący zarządzany moduł HSM.</span><span class="sxs-lookup"><span data-stu-id="ab23f-120">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="ab23f-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ab23f-121">-Name</span></span>
<span data-ttu-id="ab23f-122">Nazwa zarządzanego hsm.</span><span class="sxs-lookup"><span data-stu-id="ab23f-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="ab23f-123">- OutputPath</span><span class="sxs-lookup"><span data-stu-id="ab23f-123">-OutputPath</span></span>
<span data-ttu-id="ab23f-124">Określ ścieżkę pobierania danych domeny zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="ab23f-124">Specify the path where security domain data will be downloaded to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab23f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab23f-125">-PassThru</span></span>
<span data-ttu-id="ab23f-126">Jeśli to zwrócę, wartość logiczna zostanie zwrócona, gdy polecenie cmdlet zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="ab23f-126">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="ab23f-127">— Natłoku</span><span class="sxs-lookup"><span data-stu-id="ab23f-127">-Quorum</span></span>
<span data-ttu-id="ab23f-128">Minimalna liczba udziałów wymagana do odszyfrowania domeny zabezpieczeń na potrzeby odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="ab23f-128">The minimum number of shares required to decrypt the security domain for recovery.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab23f-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ab23f-129">-Confirm</span></span>
<span data-ttu-id="ab23f-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ab23f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab23f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab23f-131">-WhatIf</span></span>
<span data-ttu-id="ab23f-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab23f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab23f-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ab23f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab23f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab23f-134">CommonParameters</span></span>
<span data-ttu-id="ab23f-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab23f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab23f-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab23f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab23f-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab23f-137">INPUTS</span></span>

### <span data-ttu-id="ab23f-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ab23f-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="ab23f-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab23f-139">OUTPUTS</span></span>

### <span data-ttu-id="ab23f-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ab23f-140">System.Boolean</span></span>

## <span data-ttu-id="ab23f-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ab23f-141">NOTES</span></span>

## <span data-ttu-id="ab23f-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab23f-142">RELATED LINKS</span></span>
