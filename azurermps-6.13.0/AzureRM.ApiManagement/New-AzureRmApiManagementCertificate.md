---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
ms.openlocfilehash: f97f6c59bc1888f511d84ed49e6d1d49a5d7f57f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542035"
---
# <span data-ttu-id="24030-101">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="24030-101">New-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="24030-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24030-102">SYNOPSIS</span></span>
<span data-ttu-id="24030-103">Tworzy certyfikat zarządzania interfejsem API do użycia podczas uwierzytelniania z zapleczem wewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="24030-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24030-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24030-104">SYNTAX</span></span>

### <span data-ttu-id="24030-105">LoadFromFile (domyślny)</span><span class="sxs-lookup"><span data-stu-id="24030-105">LoadFromFile (Default)</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24030-106">Nowego</span><span class="sxs-lookup"><span data-stu-id="24030-106">Raw</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxBytes <Byte[]> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24030-107">Opis</span><span class="sxs-lookup"><span data-stu-id="24030-107">DESCRIPTION</span></span>
<span data-ttu-id="24030-108">Polecenie cmdlet **New-AzureRmApiManagementCertificate** tworzy certyfikat zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="24030-108">The **New-AzureRmApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="24030-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24030-109">EXAMPLES</span></span>

### <span data-ttu-id="24030-110">Przykład 1. Tworzenie i przekazywanie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="24030-110">Example 1: Create and upload a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="24030-111">To polecenie przekazuje certyfikat do zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="24030-111">This command uploads a certificate to Api Management.</span></span> <span data-ttu-id="24030-112">Tego certyfikatu można używać do wzajemnego uwierzytelniania z zapleczem przy użyciu zasad.</span><span class="sxs-lookup"><span data-stu-id="24030-112">This certificate can be used for mutual authentication with backend using policies.</span></span>

## <span data-ttu-id="24030-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24030-113">PARAMETERS</span></span>

### <span data-ttu-id="24030-114">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="24030-114">-CertificateId</span></span>
<span data-ttu-id="24030-115">Określa identyfikator certyfikatu, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="24030-115">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="24030-116">Jeśli nie określisz tego parametru, zostanie wygenerowany identyfikator.</span><span class="sxs-lookup"><span data-stu-id="24030-116">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="24030-117">-Context</span><span class="sxs-lookup"><span data-stu-id="24030-117">-Context</span></span>
<span data-ttu-id="24030-118">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="24030-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="24030-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24030-119">-DefaultProfile</span></span>
<span data-ttu-id="24030-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="24030-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24030-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="24030-121">-PfxBytes</span></span>
<span data-ttu-id="24030-122">Określa tablicę bajtów pliku certyfikatu w formacie PFX.</span><span class="sxs-lookup"><span data-stu-id="24030-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="24030-123">Ten parametr jest wymagany, jeśli nie określono parametru *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="24030-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="24030-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="24030-124">-PfxFilePath</span></span>
<span data-ttu-id="24030-125">Określa ścieżkę do pliku certyfikatu w formacie PFX do utworzenia i przekazania.</span><span class="sxs-lookup"><span data-stu-id="24030-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="24030-126">Ten parametr jest wymagany, jeśli nie określono parametru *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="24030-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24030-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="24030-127">-PfxPassword</span></span>
<span data-ttu-id="24030-128">Określa hasło dla certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="24030-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="24030-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24030-129">CommonParameters</span></span>
<span data-ttu-id="24030-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24030-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24030-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24030-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24030-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24030-132">INPUTS</span></span>

### <span data-ttu-id="24030-133">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="24030-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="24030-134">System. String</span><span class="sxs-lookup"><span data-stu-id="24030-134">System.String</span></span>

### <span data-ttu-id="24030-135">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="24030-135">System.Byte[]</span></span>

## <span data-ttu-id="24030-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24030-136">OUTPUTS</span></span>

### <span data-ttu-id="24030-137">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="24030-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="24030-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24030-138">NOTES</span></span>

## <span data-ttu-id="24030-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24030-139">RELATED LINKS</span></span>

[<span data-ttu-id="24030-140">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="24030-140">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="24030-141">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="24030-141">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="24030-142">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="24030-142">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


