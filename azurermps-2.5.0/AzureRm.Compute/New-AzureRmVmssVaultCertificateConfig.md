---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssvaultcertificateconfig
schema: 2.0.0
ms.openlocfilehash: 9ae4e22cde856129d21965b7e7f2fc9af647572a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898969"
---
# <span data-ttu-id="8308a-101">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="8308a-101">New-AzureRmVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="8308a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8308a-102">SYNOPSIS</span></span>
<span data-ttu-id="8308a-103">Umożliwia utworzenie konfiguracji certyfikatu magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="8308a-103">Creates a Key Vault certificate configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8308a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8308a-104">SYNTAX</span></span>

```
New-AzureRmVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8308a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8308a-105">DESCRIPTION</span></span>
<span data-ttu-id="8308a-106">Polecenie cmdlet **New-AzureRmVmssVaultCertificateConfig** określa klucz tajny, który należy umieścić na maszynach wirtualnych zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="8308a-106">The **New-AzureRmVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="8308a-107">Dane wyjściowe tego polecenia cmdlet są przeznaczone do użycia z poleceniem cmdlet Add-AzureRmVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="8308a-107">The output of this cmdlet is intended to be used with the Add-AzureRmVmssSecret cmdlet.</span></span>

## <span data-ttu-id="8308a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8308a-108">EXAMPLES</span></span>

### <span data-ttu-id="8308a-109">Przykład 1: Tworzenie konfiguracji certyfikatu magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="8308a-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="8308a-110">To polecenie powoduje utworzenie konfiguracji certyfikatu magazynu kluczy, w której jest używany magazyn certyfikatów o nazwie Moje certyfikaty znajdujący się pod określonym adresem URL certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="8308a-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="8308a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8308a-111">PARAMETERS</span></span>

### <span data-ttu-id="8308a-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="8308a-112">-CertificateStore</span></span>
<span data-ttu-id="8308a-113">Określa magazyn certyfikatów na maszynach wirtualnych w zestawie skali, w którym jest dodawany certyfikat.</span><span class="sxs-lookup"><span data-stu-id="8308a-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="8308a-114">Jest to prawidłowe tylko w przypadku zestawów skali maszyny wirtualnej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="8308a-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

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

### <span data-ttu-id="8308a-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="8308a-115">-CertificateUrl</span></span>
<span data-ttu-id="8308a-116">Określa identyfikator URI certyfikatu przechowywanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="8308a-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>

<span data-ttu-id="8308a-117">Jest to kodowanie Base64 następującego obiektu JSON zakodowanego w formacie UTF-8:</span><span class="sxs-lookup"><span data-stu-id="8308a-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8:</span></span>


<span data-ttu-id="8308a-118">{"dane": " \<Base64-encoded-certificate\> ", "DataType": "PFX", "hasło": " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="8308a-118">{ "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

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

### <span data-ttu-id="8308a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8308a-119">-DefaultProfile</span></span>
<span data-ttu-id="8308a-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8308a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8308a-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8308a-121">-Confirm</span></span>
<span data-ttu-id="8308a-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8308a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8308a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8308a-123">-WhatIf</span></span>
<span data-ttu-id="8308a-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8308a-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8308a-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8308a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8308a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8308a-126">CommonParameters</span></span>
<span data-ttu-id="8308a-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8308a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8308a-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8308a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8308a-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8308a-129">INPUTS</span></span>

### <span data-ttu-id="8308a-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8308a-130">None</span></span>
<span data-ttu-id="8308a-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="8308a-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8308a-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8308a-132">OUTPUTS</span></span>

###  
<span data-ttu-id="8308a-133">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="8308a-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="8308a-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8308a-134">NOTES</span></span>

## <span data-ttu-id="8308a-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8308a-135">RELATED LINKS</span></span>

[<span data-ttu-id="8308a-136">Dodaj-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="8308a-136">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)
