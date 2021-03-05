---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
ms.openlocfilehash: bb60ce1fc2cb20a24d1b445cf4a3729bf26747ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965441"
---
# <span data-ttu-id="cf941-101">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="cf941-101">Set-AzApiManagementCertificate</span></span>

## <span data-ttu-id="cf941-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf941-102">SYNOPSIS</span></span>
<span data-ttu-id="cf941-103">Modyfikuje certyfikat zarządzania interfejsem API, który jest skonfigurowany do wymusze uwierzytelniania za pomocą zaplecza.</span><span class="sxs-lookup"><span data-stu-id="cf941-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

## <span data-ttu-id="cf941-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cf941-104">SYNTAX</span></span>

### <span data-ttu-id="cf941-105">LoadFromFile (domyślne)</span><span class="sxs-lookup"><span data-stu-id="cf941-105">LoadFromFile (Default)</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxFilePath <String>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf941-106">Nieprzetworzone</span><span class="sxs-lookup"><span data-stu-id="cf941-106">Raw</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxBytes <Byte[]>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf941-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="cf941-107">DESCRIPTION</span></span>
<span data-ttu-id="cf941-108">Polecenie **cmdlet Set-AzApiManagementCertificate** modyfikuje certyfikat usługi Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="cf941-108">The **Set-AzApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="cf941-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cf941-109">EXAMPLES</span></span>

### <span data-ttu-id="cf941-110">Przykład 1. Modyfikowanie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="cf941-110">Example 1: Modify a certificate</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="cf941-111">To polecenie modyfikuje określony certyfikat zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="cf941-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="cf941-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf941-112">PARAMETERS</span></span>

### <span data-ttu-id="cf941-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="cf941-113">-CertificateId</span></span>
<span data-ttu-id="cf941-114">Określa identyfikator certyfikatu do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="cf941-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="cf941-115">— kontekst</span><span class="sxs-lookup"><span data-stu-id="cf941-115">-Context</span></span>
<span data-ttu-id="cf941-116">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="cf941-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="cf941-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf941-117">-DefaultProfile</span></span>
<span data-ttu-id="cf941-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cf941-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf941-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf941-119">-PassThru</span></span>
<span data-ttu-id="cf941-120">passthru</span><span class="sxs-lookup"><span data-stu-id="cf941-120">passthru</span></span>

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

### <span data-ttu-id="cf941-121">- PfxBytes</span><span class="sxs-lookup"><span data-stu-id="cf941-121">-PfxBytes</span></span>
<span data-ttu-id="cf941-122">Określa tablicę bajtów pliku certyfikatu w formacie pfx.</span><span class="sxs-lookup"><span data-stu-id="cf941-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="cf941-123">Ten parametr jest wymagany, jeśli nie określisz *parametru PfxFilePath.*</span><span class="sxs-lookup"><span data-stu-id="cf941-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="cf941-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="cf941-124">-PfxFilePath</span></span>
<span data-ttu-id="cf941-125">Określa ścieżkę do pliku certyfikatu w formacie pfx do utworzenia i przekazania.</span><span class="sxs-lookup"><span data-stu-id="cf941-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="cf941-126">Ten parametr jest wymagany, jeśli nie określisz *parametru PfxBytes.*</span><span class="sxs-lookup"><span data-stu-id="cf941-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="cf941-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="cf941-127">-PfxPassword</span></span>
<span data-ttu-id="cf941-128">Określa hasło certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="cf941-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="cf941-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf941-129">CommonParameters</span></span>
<span data-ttu-id="cf941-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf941-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf941-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf941-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf941-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf941-132">INPUTS</span></span>

### <span data-ttu-id="cf941-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cf941-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cf941-134">System.String</span><span class="sxs-lookup"><span data-stu-id="cf941-134">System.String</span></span>

### <span data-ttu-id="cf941-135">System.Byte[]</span><span class="sxs-lookup"><span data-stu-id="cf941-135">System.Byte[]</span></span>

### <span data-ttu-id="cf941-136">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="cf941-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cf941-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf941-137">OUTPUTS</span></span>

### <span data-ttu-id="cf941-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="cf941-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="cf941-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cf941-139">NOTES</span></span>

## <span data-ttu-id="cf941-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf941-140">RELATED LINKS</span></span>

[<span data-ttu-id="cf941-141">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="cf941-141">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="cf941-142">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="cf941-142">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="cf941-143">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="cf941-143">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)


