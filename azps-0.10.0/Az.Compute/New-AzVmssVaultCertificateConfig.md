---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: 0889bfa5abfdf90480eb508ebad7a62607912722
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893597"
---
# <span data-ttu-id="428bc-101">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="428bc-101">New-AzVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="428bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="428bc-102">SYNOPSIS</span></span>
<span data-ttu-id="428bc-103">Umożliwia utworzenie konfiguracji certyfikatu magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="428bc-103">Creates a Key Vault certificate configuration.</span></span>

## <span data-ttu-id="428bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="428bc-104">SYNTAX</span></span>

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="428bc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="428bc-105">DESCRIPTION</span></span>
<span data-ttu-id="428bc-106">Polecenie cmdlet **New-AzVmssVaultCertificateConfig** określa klucz tajny, który należy umieścić na maszynach wirtualnych zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="428bc-106">The **New-AzVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="428bc-107">Dane wyjściowe tego polecenia cmdlet są przeznaczone do użycia z poleceniem cmdlet Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="428bc-107">The output of this cmdlet is intended to be used with the Add-AzVmssSecret cmdlet.</span></span>

## <span data-ttu-id="428bc-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="428bc-108">EXAMPLES</span></span>

### <span data-ttu-id="428bc-109">Przykład 1: Tworzenie konfiguracji certyfikatu magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="428bc-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="428bc-110">To polecenie powoduje utworzenie konfiguracji certyfikatu magazynu kluczy, w której jest używany magazyn certyfikatów o nazwie Moje certyfikaty znajdujący się pod określonym adresem URL certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="428bc-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="428bc-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="428bc-111">PARAMETERS</span></span>

### <span data-ttu-id="428bc-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="428bc-112">-CertificateStore</span></span>
<span data-ttu-id="428bc-113">Określa magazyn certyfikatów na maszynach wirtualnych w zestawie skali, w którym jest dodawany certyfikat.</span><span class="sxs-lookup"><span data-stu-id="428bc-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="428bc-114">Jest to prawidłowe tylko w przypadku zestawów skali maszyny wirtualnej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="428bc-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="428bc-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="428bc-115">-CertificateUrl</span></span>
<span data-ttu-id="428bc-116">Określa identyfikator URI certyfikatu przechowywanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="428bc-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>

<span data-ttu-id="428bc-117">Jest to kodowanie Base64 następującego obiektu JSON zakodowanego w formacie UTF-8:</span><span class="sxs-lookup"><span data-stu-id="428bc-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8:</span></span>


<span data-ttu-id="428bc-118">{"dane": " \< Kodowanie Base64-Certificate " \> ," DataType ":" PFX "," Password ":" \< PFX-File-Password \> "}</span><span class="sxs-lookup"><span data-stu-id="428bc-118">{ "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="428bc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="428bc-119">-DefaultProfile</span></span>
<span data-ttu-id="428bc-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="428bc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="428bc-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="428bc-121">-Confirm</span></span>
<span data-ttu-id="428bc-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="428bc-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="428bc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="428bc-123">-WhatIf</span></span>
<span data-ttu-id="428bc-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="428bc-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="428bc-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="428bc-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="428bc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="428bc-126">CommonParameters</span></span>
<span data-ttu-id="428bc-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="428bc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="428bc-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="428bc-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="428bc-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="428bc-129">INPUTS</span></span>

### <span data-ttu-id="428bc-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="428bc-130">None</span></span>
<span data-ttu-id="428bc-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="428bc-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="428bc-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="428bc-132">OUTPUTS</span></span>

###  
<span data-ttu-id="428bc-133">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="428bc-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="428bc-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="428bc-134">NOTES</span></span>

## <span data-ttu-id="428bc-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="428bc-135">RELATED LINKS</span></span>

[<span data-ttu-id="428bc-136">Dodaj-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="428bc-136">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)
