---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 55b95cec3e699872688fad5daeb0d2f7e89059c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547211"
---
# <span data-ttu-id="00131-101">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="00131-101">New-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="00131-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="00131-102">SYNOPSIS</span></span>
<span data-ttu-id="00131-103">Tworzy certyfikat zarządzania interfejsem API do użycia podczas uwierzytelniania z zapleczem wewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="00131-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00131-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="00131-104">SYNTAX</span></span>

### <span data-ttu-id="00131-105">Ładowanie z pliku (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="00131-105">Load from file (Default)</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00131-106">Nowego</span><span class="sxs-lookup"><span data-stu-id="00131-106">Raw</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxBytes <Byte[]> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00131-107">Opis</span><span class="sxs-lookup"><span data-stu-id="00131-107">DESCRIPTION</span></span>
<span data-ttu-id="00131-108">Polecenie cmdlet **New-AzureRmApiManagementCertificate** tworzy certyfikat zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="00131-108">The **New-AzureRmApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="00131-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="00131-109">EXAMPLES</span></span>

### <span data-ttu-id="00131-110">Przykład 1. Tworzenie i przekazywanie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="00131-110">Example 1: Create and upload a certificate</span></span>
```
PS C:\>New-AzureRmApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="00131-111">To polecenie tworzy certyfikat zarządzania interfejsem API i przekazuje go.</span><span class="sxs-lookup"><span data-stu-id="00131-111">This command creates an API Management certificate and uploads it.</span></span>

## <span data-ttu-id="00131-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="00131-112">PARAMETERS</span></span>

### <span data-ttu-id="00131-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="00131-113">-CertificateId</span></span>
<span data-ttu-id="00131-114">Określa identyfikator certyfikatu, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="00131-114">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="00131-115">Jeśli nie określisz tego parametru, zostanie wygenerowany identyfikator.</span><span class="sxs-lookup"><span data-stu-id="00131-115">If you do not specify this parameter, an ID is generated for you.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00131-116">-Context</span><span class="sxs-lookup"><span data-stu-id="00131-116">-Context</span></span>
<span data-ttu-id="00131-117">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="00131-117">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00131-118">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="00131-118">-PfxBytes</span></span>
<span data-ttu-id="00131-119">Określa tablicę bajtów pliku certyfikatu w formacie PFX.</span><span class="sxs-lookup"><span data-stu-id="00131-119">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="00131-120">Ten parametr jest wymagany, jeśli nie określono parametru *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="00131-120">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: Raw
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00131-121">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="00131-121">-PfxFilePath</span></span>
<span data-ttu-id="00131-122">Określa ścieżkę do pliku certyfikatu w formacie PFX do utworzenia i przekazania.</span><span class="sxs-lookup"><span data-stu-id="00131-122">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="00131-123">Ten parametr jest wymagany, jeśli nie określono parametru *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="00131-123">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Load from file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00131-124">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="00131-124">-PfxPassword</span></span>
<span data-ttu-id="00131-125">Określa hasło dla certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="00131-125">Specifies the password for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00131-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00131-126">-DefaultProfile</span></span>
<span data-ttu-id="00131-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="00131-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00131-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00131-128">CommonParameters</span></span>
<span data-ttu-id="00131-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00131-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00131-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00131-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00131-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00131-131">INPUTS</span></span>

## <span data-ttu-id="00131-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="00131-132">OUTPUTS</span></span>

### <span data-ttu-id="00131-133">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="00131-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="00131-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="00131-134">NOTES</span></span>

## <span data-ttu-id="00131-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00131-135">RELATED LINKS</span></span>

[<span data-ttu-id="00131-136">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="00131-136">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="00131-137">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="00131-137">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="00131-138">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="00131-138">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


