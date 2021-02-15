---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: 23b2b3acd5bb15771d3383cc39c6e0a69073a750
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177635"
---
# <span data-ttu-id="1d223-101">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="1d223-101">New-AzVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="1d223-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d223-102">SYNOPSIS</span></span>
<span data-ttu-id="1d223-103">Tworzy konfigurację certyfikatu magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="1d223-103">Creates a Key Vault certificate configuration.</span></span>

## <span data-ttu-id="1d223-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1d223-104">SYNTAX</span></span>

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d223-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1d223-105">DESCRIPTION</span></span>
<span data-ttu-id="1d223-106">Polecenie cmdlet **New-AzVmssVaultCertificateConfig** określa klucz tajny, który musi zostać umieszczony na komputerach wirtualnych z zestawem skal maszyny wirtualnej (VIRTUAL Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="1d223-106">The **New-AzVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="1d223-107">Dane wyjściowe tego polecenia cmdlet mają być używane z Add-AzVmssSecret cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d223-107">The output of this cmdlet is intended to be used with the Add-AzVmssSecret cmdlet.</span></span>

## <span data-ttu-id="1d223-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1d223-108">EXAMPLES</span></span>

### <span data-ttu-id="1d223-109">Przykład 1. Tworzenie konfiguracji certyfikatu magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="1d223-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="1d223-110">To polecenie tworzy konfigurację certyfikatu magazynu kluczy, która korzysta z magazynu certyfikatów o nazwie MyCerts znajdującego się pod adresem URL określonego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="1d223-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="1d223-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d223-111">PARAMETERS</span></span>

### <span data-ttu-id="1d223-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="1d223-112">-CertificateStore</span></span>
<span data-ttu-id="1d223-113">Określa magazyn certyfikatów na komputerach wirtualnych w zestawie skali, w którym certyfikat jest dodawany.</span><span class="sxs-lookup"><span data-stu-id="1d223-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="1d223-114">Ta funkcja jest prawidłowa tylko w przypadku zestawów skal dla maszyn wirtualnych systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="1d223-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d223-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="1d223-115">-CertificateUrl</span></span>
<span data-ttu-id="1d223-116">Określa URI certyfikatu przechowywanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="1d223-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>
<span data-ttu-id="1d223-117">Jest to kodowanie base64 następującego obiektu JSON, które jest zakodowane w utf-8: { "data":" \<Base64-encoded-certificate\> ", "dataType":"pfx", "password":" \<pfx-file-password\> }</span><span class="sxs-lookup"><span data-stu-id="1d223-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8: { "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d223-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d223-118">-DefaultProfile</span></span>
<span data-ttu-id="1d223-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1d223-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d223-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1d223-120">-Confirm</span></span>
<span data-ttu-id="1d223-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1d223-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d223-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d223-122">-WhatIf</span></span>
<span data-ttu-id="1d223-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d223-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1d223-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1d223-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d223-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d223-125">CommonParameters</span></span>
<span data-ttu-id="1d223-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d223-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d223-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d223-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d223-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d223-128">INPUTS</span></span>

### <span data-ttu-id="1d223-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1d223-129">System.String</span></span>

## <span data-ttu-id="1d223-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1d223-130">OUTPUTS</span></span>

### <span data-ttu-id="1d223-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="1d223-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span></span>

## <span data-ttu-id="1d223-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1d223-132">NOTES</span></span>

## <span data-ttu-id="1d223-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d223-133">RELATED LINKS</span></span>

[<span data-ttu-id="1d223-134">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="1d223-134">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)
