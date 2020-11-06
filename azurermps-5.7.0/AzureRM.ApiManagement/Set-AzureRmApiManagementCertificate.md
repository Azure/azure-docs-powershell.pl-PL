---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 1b1f16c8d48debb04ad1f38c03aa58e65f9953a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545839"
---
# <span data-ttu-id="a561f-101">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="a561f-101">Set-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="a561f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a561f-102">SYNOPSIS</span></span>
<span data-ttu-id="a561f-103">Modyfikuje certyfikat zarządzania interfejsem API, który jest skonfigurowany dla wzajemnego uwierzytelniania z zapleczem wewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="a561f-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a561f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a561f-104">SYNTAX</span></span>

### <span data-ttu-id="a561f-105">LoadFromFile (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a561f-105">LoadFromFile (Default)</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxFilePath <String> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a561f-106">Nowego</span><span class="sxs-lookup"><span data-stu-id="a561f-106">Raw</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxBytes <Byte[]> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a561f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a561f-107">DESCRIPTION</span></span>
<span data-ttu-id="a561f-108">Polecenie cmdlet **Set-AzureRmApiManagementCertificate** modyfikuje certyfikat zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="a561f-108">The **Set-AzureRmApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="a561f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a561f-109">EXAMPLES</span></span>

### <span data-ttu-id="a561f-110">Przykład 1. Modyfikowanie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="a561f-110">Example 1: Modify a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="a561f-111">To polecenie modyfikuje określony certyfikat zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="a561f-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="a561f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a561f-112">PARAMETERS</span></span>

### <span data-ttu-id="a561f-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="a561f-113">-CertificateId</span></span>
<span data-ttu-id="a561f-114">Określa identyfikator certyfikatu do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="a561f-114">Specifies the ID of the certificate to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a561f-115">-Context</span><span class="sxs-lookup"><span data-stu-id="a561f-115">-Context</span></span>
<span data-ttu-id="a561f-116">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a561f-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a561f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a561f-117">-DefaultProfile</span></span>
<span data-ttu-id="a561f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a561f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="a561f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a561f-119">-PassThru</span></span>
<span data-ttu-id="a561f-120">passthru</span><span class="sxs-lookup"><span data-stu-id="a561f-120">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a561f-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="a561f-121">-PfxBytes</span></span>
<span data-ttu-id="a561f-122">Określa tablicę bajtów pliku certyfikatu w formacie PFX.</span><span class="sxs-lookup"><span data-stu-id="a561f-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="a561f-123">Ten parametr jest wymagany, jeśli nie określono parametru *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="a561f-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

```yaml
Type: Byte[]
Parameter Sets: Raw
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a561f-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="a561f-124">-PfxFilePath</span></span>
<span data-ttu-id="a561f-125">Określa ścieżkę do pliku certyfikatu w formacie PFX do utworzenia i przekazania.</span><span class="sxs-lookup"><span data-stu-id="a561f-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="a561f-126">Ten parametr jest wymagany, jeśli nie określono parametru *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="a561f-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: String
Parameter Sets: LoadFromFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a561f-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="a561f-127">-PfxPassword</span></span>
<span data-ttu-id="a561f-128">Określa hasło dla certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="a561f-128">Specifies the password for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a561f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a561f-129">CommonParameters</span></span>
<span data-ttu-id="a561f-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a561f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a561f-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a561f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a561f-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a561f-132">INPUTS</span></span>

### <span data-ttu-id="a561f-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a561f-133">None</span></span>
<span data-ttu-id="a561f-134">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="a561f-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a561f-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a561f-135">OUTPUTS</span></span>

### <span data-ttu-id="a561f-136">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="a561f-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="a561f-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a561f-137">NOTES</span></span>

## <span data-ttu-id="a561f-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a561f-138">RELATED LINKS</span></span>

[<span data-ttu-id="a561f-139">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="a561f-139">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="a561f-140">Nowe — AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="a561f-140">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="a561f-141">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="a561f-141">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)


