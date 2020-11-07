---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
ms.openlocfilehash: b565c616ff493b2721486bc6916238e997397ce6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869351"
---
# <span data-ttu-id="18744-101">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="18744-101">Set-AzApiManagementCertificate</span></span>

## <span data-ttu-id="18744-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="18744-102">SYNOPSIS</span></span>
<span data-ttu-id="18744-103">Modyfikuje certyfikat zarządzania interfejsem API, który jest skonfigurowany dla wzajemnego uwierzytelniania z zapleczem wewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="18744-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

## <span data-ttu-id="18744-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="18744-104">SYNTAX</span></span>

### <span data-ttu-id="18744-105">LoadFromFile (domyślny)</span><span class="sxs-lookup"><span data-stu-id="18744-105">LoadFromFile (Default)</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxFilePath <String>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18744-106">Nowego</span><span class="sxs-lookup"><span data-stu-id="18744-106">Raw</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxBytes <Byte[]>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18744-107">Opis</span><span class="sxs-lookup"><span data-stu-id="18744-107">DESCRIPTION</span></span>
<span data-ttu-id="18744-108">Polecenie cmdlet **Set-AzApiManagementCertificate** modyfikuje certyfikat zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="18744-108">The **Set-AzApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="18744-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="18744-109">EXAMPLES</span></span>

### <span data-ttu-id="18744-110">Przykład 1. Modyfikowanie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="18744-110">Example 1: Modify a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="18744-111">To polecenie modyfikuje określony certyfikat zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="18744-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="18744-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="18744-112">PARAMETERS</span></span>

### <span data-ttu-id="18744-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="18744-113">-CertificateId</span></span>
<span data-ttu-id="18744-114">Określa identyfikator certyfikatu do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="18744-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="18744-115">-Context</span><span class="sxs-lookup"><span data-stu-id="18744-115">-Context</span></span>
<span data-ttu-id="18744-116">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="18744-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="18744-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18744-117">-DefaultProfile</span></span>
<span data-ttu-id="18744-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="18744-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18744-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18744-119">-PassThru</span></span>
<span data-ttu-id="18744-120">passthru</span><span class="sxs-lookup"><span data-stu-id="18744-120">passthru</span></span>

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

### <span data-ttu-id="18744-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="18744-121">-PfxBytes</span></span>
<span data-ttu-id="18744-122">Określa tablicę bajtów pliku certyfikatu w formacie PFX.</span><span class="sxs-lookup"><span data-stu-id="18744-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="18744-123">Ten parametr jest wymagany, jeśli nie określono parametru *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="18744-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="18744-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="18744-124">-PfxFilePath</span></span>
<span data-ttu-id="18744-125">Określa ścieżkę do pliku certyfikatu w formacie PFX do utworzenia i przekazania.</span><span class="sxs-lookup"><span data-stu-id="18744-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="18744-126">Ten parametr jest wymagany, jeśli nie określono parametru *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="18744-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="18744-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="18744-127">-PfxPassword</span></span>
<span data-ttu-id="18744-128">Określa hasło dla certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="18744-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="18744-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18744-129">CommonParameters</span></span>
<span data-ttu-id="18744-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18744-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18744-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18744-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18744-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18744-132">INPUTS</span></span>

### <span data-ttu-id="18744-133">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="18744-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="18744-134">System. String</span><span class="sxs-lookup"><span data-stu-id="18744-134">System.String</span></span>

### <span data-ttu-id="18744-135">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="18744-135">System.Byte[]</span></span>

### <span data-ttu-id="18744-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="18744-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="18744-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="18744-137">OUTPUTS</span></span>

### <span data-ttu-id="18744-138">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="18744-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="18744-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="18744-139">NOTES</span></span>

## <span data-ttu-id="18744-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18744-140">RELATED LINKS</span></span>

[<span data-ttu-id="18744-141">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="18744-141">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="18744-142">Nowe — AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="18744-142">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="18744-143">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="18744-143">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)


