---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
ms.openlocfilehash: ca9305b2d5863276c5d898e310dfab8be7488382
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718748"
---
# <span data-ttu-id="82cf6-101">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="82cf6-101">Set-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="82cf6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="82cf6-102">SYNOPSIS</span></span>
<span data-ttu-id="82cf6-103">Modyfikuje certyfikat zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="82cf6-103">Modifies an API Management certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82cf6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="82cf6-104">SYNTAX</span></span>

### <span data-ttu-id="82cf6-105">Ładowanie z pliku (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="82cf6-105">Load from file (Default)</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxFilePath <String> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82cf6-106">Nowego</span><span class="sxs-lookup"><span data-stu-id="82cf6-106">Raw</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxBytes <Byte[]> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="82cf6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="82cf6-107">DESCRIPTION</span></span>
<span data-ttu-id="82cf6-108">Polecenie cmdlet **Set-AzureRmApiManagementCertificate** modyfikuje certyfikat zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="82cf6-108">The **Set-AzureRmApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="82cf6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="82cf6-109">EXAMPLES</span></span>

### <span data-ttu-id="82cf6-110">Przykład 1. Modyfikowanie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="82cf6-110">Example 1: Modify a certificate</span></span>
```
PS C:\>Set-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="82cf6-111">To polecenie modyfikuje określony certyfikat zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="82cf6-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="82cf6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="82cf6-112">PARAMETERS</span></span>

### <span data-ttu-id="82cf6-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="82cf6-113">-CertificateId</span></span>
<span data-ttu-id="82cf6-114">Określa identyfikator certyfikatu do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="82cf6-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="82cf6-115">-Context</span><span class="sxs-lookup"><span data-stu-id="82cf6-115">-Context</span></span>
<span data-ttu-id="82cf6-116">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="82cf6-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="82cf6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82cf6-117">-PassThru</span></span>
<span data-ttu-id="82cf6-118">passthru</span><span class="sxs-lookup"><span data-stu-id="82cf6-118">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82cf6-119">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="82cf6-119">-PfxBytes</span></span>
<span data-ttu-id="82cf6-120">Określa tablicę bajtów pliku certyfikatu w formacie PFX.</span><span class="sxs-lookup"><span data-stu-id="82cf6-120">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="82cf6-121">Ten parametr jest wymagany, jeśli nie określono parametru *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="82cf6-121">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="82cf6-122">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="82cf6-122">-PfxFilePath</span></span>
<span data-ttu-id="82cf6-123">Określa ścieżkę do pliku certyfikatu w formacie PFX do utworzenia i przekazania.</span><span class="sxs-lookup"><span data-stu-id="82cf6-123">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="82cf6-124">Ten parametr jest wymagany, jeśli nie określono parametru *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="82cf6-124">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="82cf6-125">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="82cf6-125">-PfxPassword</span></span>
<span data-ttu-id="82cf6-126">Określa hasło dla certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="82cf6-126">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="82cf6-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82cf6-127">-DefaultProfile</span></span>
<span data-ttu-id="82cf6-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="82cf6-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82cf6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82cf6-129">CommonParameters</span></span>
<span data-ttu-id="82cf6-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82cf6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82cf6-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82cf6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82cf6-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82cf6-132">INPUTS</span></span>

## <span data-ttu-id="82cf6-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="82cf6-133">OUTPUTS</span></span>

### <span data-ttu-id="82cf6-134">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="82cf6-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="82cf6-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="82cf6-135">NOTES</span></span>

## <span data-ttu-id="82cf6-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82cf6-136">RELATED LINKS</span></span>

[<span data-ttu-id="82cf6-137">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="82cf6-137">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="82cf6-138">Nowe — AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="82cf6-138">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="82cf6-139">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="82cf6-139">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)


