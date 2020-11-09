---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsmsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmSecurityDomain.md
ms.openlocfilehash: 10a54afa8a6ef2e37beebd9d6cdcd304b2d13979
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304621"
---
# <span data-ttu-id="576ff-101">Backup-AzManagedHsmSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="576ff-101">Backup-AzManagedHsmSecurityDomain</span></span>

## <span data-ttu-id="576ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="576ff-102">SYNOPSIS</span></span>
<span data-ttu-id="576ff-103">Wykonuje kopię zapasową danych domeny zabezpieczeń zarządzanego modułu HSM w celu przywracania.</span><span class="sxs-lookup"><span data-stu-id="576ff-103">Backs up the security domain data of a managed HSM for restoring.</span></span>

## <span data-ttu-id="576ff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="576ff-104">SYNTAX</span></span>

### <span data-ttu-id="576ff-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="576ff-105">ByName (Default)</span></span>
```
Backup-AzManagedHsmSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="576ff-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="576ff-106">ByInputObject</span></span>
```
Backup-AzManagedHsmSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="576ff-107">Opis</span><span class="sxs-lookup"><span data-stu-id="576ff-107">DESCRIPTION</span></span>
<span data-ttu-id="576ff-108">To polecenie cmdlet wykonuje kopię zapasową danych domeny zabezpieczeń zarządzanego modułu HSM w celu przywracania.</span><span class="sxs-lookup"><span data-stu-id="576ff-108">This cmdlet backs up the security domain data of a managed HSM for restoring.</span></span>

## <span data-ttu-id="576ff-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="576ff-109">EXAMPLES</span></span>

### <span data-ttu-id="576ff-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="576ff-110">Example 1</span></span>
```powershell
PS C:\Users\username\> Backup-AzManagedHsmSecurityDomain -Name testmhsm -Certificates {pathOfCertificates}/sd1.cer, {pathOfCertificates}/sd2.cer, {pathOfCertificates}/sd3.cer -OutputPath {pathOfOutput}/sd.ps.json -Quorum 2
```

<span data-ttu-id="576ff-111">To polecenie umożliwia pobranie zarządzanego modułu HSM o nazwie testmhsm i zapisanie kopii zapasowej tej domeny zabezpieczeń modułu HSM w określonym pliku wyjściowym.</span><span class="sxs-lookup"><span data-stu-id="576ff-111">This command retrieves the managed HSM named testmhsm and saves a backup of that managed HSM security domain to the specified output file.</span></span>

## <span data-ttu-id="576ff-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="576ff-112">PARAMETERS</span></span>

### <span data-ttu-id="576ff-113">-Certificates</span><span class="sxs-lookup"><span data-stu-id="576ff-113">-Certificates</span></span>
<span data-ttu-id="576ff-114">Ścieżki do certyfikatów używanych do szyfrowania danych domeny zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="576ff-114">Paths to the certificates that are used to encrypt the security domain data.</span></span>

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

### <span data-ttu-id="576ff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="576ff-115">-DefaultProfile</span></span>
<span data-ttu-id="576ff-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="576ff-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="576ff-117">-Force</span><span class="sxs-lookup"><span data-stu-id="576ff-117">-Force</span></span>
<span data-ttu-id="576ff-118">Określ, czy zastąpić istniejący plik.</span><span class="sxs-lookup"><span data-stu-id="576ff-118">Specify whether to overwrite existing file.</span></span>

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

### <span data-ttu-id="576ff-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="576ff-119">-InputObject</span></span>
<span data-ttu-id="576ff-120">Obiekt reprezentujący zarządzany element HSM.</span><span class="sxs-lookup"><span data-stu-id="576ff-120">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="576ff-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="576ff-121">-Name</span></span>
<span data-ttu-id="576ff-122">Nazwa zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="576ff-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="576ff-123">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="576ff-123">-OutputPath</span></span>
<span data-ttu-id="576ff-124">Określ ścieżkę, do której mają być pobierane dane domeny zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="576ff-124">Specify the path where security domain data will be downloaded to.</span></span>

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

### <span data-ttu-id="576ff-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="576ff-125">-PassThru</span></span>
<span data-ttu-id="576ff-126">Po określeniu wartość logiczna zostanie zwrócona, gdy polecenie cmdlet zostanie wykonane pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="576ff-126">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="576ff-127">-Kworum</span><span class="sxs-lookup"><span data-stu-id="576ff-127">-Quorum</span></span>
<span data-ttu-id="576ff-128">Minimalna liczba akcji wymaganych do odszyfrowania domeny zabezpieczeń na potrzeby odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="576ff-128">The minimum number of shares required to decrypt the security domain for recovery.</span></span>

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

### <span data-ttu-id="576ff-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="576ff-129">-Confirm</span></span>
<span data-ttu-id="576ff-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="576ff-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="576ff-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="576ff-131">-WhatIf</span></span>
<span data-ttu-id="576ff-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="576ff-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="576ff-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="576ff-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="576ff-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="576ff-134">CommonParameters</span></span>
<span data-ttu-id="576ff-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="576ff-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="576ff-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="576ff-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="576ff-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="576ff-137">INPUTS</span></span>

### <span data-ttu-id="576ff-138">Microsoft. Azure. Commands. platforming. models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="576ff-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="576ff-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="576ff-139">OUTPUTS</span></span>

### <span data-ttu-id="576ff-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="576ff-140">System.Boolean</span></span>

## <span data-ttu-id="576ff-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="576ff-141">NOTES</span></span>

## <span data-ttu-id="576ff-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="576ff-142">RELATED LINKS</span></span>
