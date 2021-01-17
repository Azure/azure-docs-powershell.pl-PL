---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
ms.openlocfilehash: 3c31da297b47c5d35c7d7b4eea5c55ca87d9521d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335389"
---
# <span data-ttu-id="36335-101">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="36335-101">Set-AzApiManagementCertificate</span></span>

## <span data-ttu-id="36335-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36335-102">SYNOPSIS</span></span>
<span data-ttu-id="36335-103">Modyfikuje certyfikat zarządzania interfejsem API, który jest skonfigurowany dla wzajemnego uwierzytelniania z zapleczem wewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="36335-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

## <span data-ttu-id="36335-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36335-104">SYNTAX</span></span>

### <span data-ttu-id="36335-105">LoadFromFile (domyślny)</span><span class="sxs-lookup"><span data-stu-id="36335-105">LoadFromFile (Default)</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxFilePath <String>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36335-106">Nowego</span><span class="sxs-lookup"><span data-stu-id="36335-106">Raw</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxBytes <Byte[]>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36335-107">Opis</span><span class="sxs-lookup"><span data-stu-id="36335-107">DESCRIPTION</span></span>
<span data-ttu-id="36335-108">Polecenie cmdlet **Set-AzApiManagementCertificate** modyfikuje certyfikat zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="36335-108">The **Set-AzApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="36335-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36335-109">EXAMPLES</span></span>

### <span data-ttu-id="36335-110">Przykład 1. Modyfikowanie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="36335-110">Example 1: Modify a certificate</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="36335-111">To polecenie modyfikuje określony certyfikat zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="36335-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="36335-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36335-112">PARAMETERS</span></span>

### <span data-ttu-id="36335-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="36335-113">-CertificateId</span></span>
<span data-ttu-id="36335-114">Określa identyfikator certyfikatu do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="36335-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="36335-115">-Context</span><span class="sxs-lookup"><span data-stu-id="36335-115">-Context</span></span>
<span data-ttu-id="36335-116">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="36335-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36335-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36335-117">-DefaultProfile</span></span>
<span data-ttu-id="36335-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="36335-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36335-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36335-119">-PassThru</span></span>
<span data-ttu-id="36335-120">passthru</span><span class="sxs-lookup"><span data-stu-id="36335-120">passthru</span></span>

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

### <span data-ttu-id="36335-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="36335-121">-PfxBytes</span></span>
<span data-ttu-id="36335-122">Określa tablicę bajtów pliku certyfikatu w formacie PFX.</span><span class="sxs-lookup"><span data-stu-id="36335-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="36335-123">Ten parametr jest wymagany, jeśli nie określono parametru *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="36335-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="36335-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="36335-124">-PfxFilePath</span></span>
<span data-ttu-id="36335-125">Określa ścieżkę do pliku certyfikatu w formacie PFX do utworzenia i przekazania.</span><span class="sxs-lookup"><span data-stu-id="36335-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="36335-126">Ten parametr jest wymagany, jeśli nie określono parametru *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="36335-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="36335-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="36335-127">-PfxPassword</span></span>
<span data-ttu-id="36335-128">Określa hasło dla certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="36335-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="36335-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36335-129">CommonParameters</span></span>
<span data-ttu-id="36335-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36335-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36335-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36335-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36335-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36335-132">INPUTS</span></span>

### <span data-ttu-id="36335-133">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="36335-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="36335-134">System. String</span><span class="sxs-lookup"><span data-stu-id="36335-134">System.String</span></span>

### <span data-ttu-id="36335-135">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="36335-135">System.Byte[]</span></span>

### <span data-ttu-id="36335-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="36335-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="36335-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36335-137">OUTPUTS</span></span>

### <span data-ttu-id="36335-138">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="36335-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="36335-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36335-139">NOTES</span></span>

## <span data-ttu-id="36335-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36335-140">RELATED LINKS</span></span>

[<span data-ttu-id="36335-141">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="36335-141">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="36335-142">Nowe — AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="36335-142">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="36335-143">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="36335-143">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)


