---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
ms.openlocfilehash: 657a1b729bfa5de8b62c58ed590b5cbf2cf7dca8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195363"
---
# <span data-ttu-id="8bc95-101">New-AzApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="8bc95-101">New-AzApiManagementSystemCertificate</span></span>

## <span data-ttu-id="8bc95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bc95-102">SYNOPSIS</span></span>
<span data-ttu-id="8bc95-103">Tworzy `PsApiManagementSystemCertificate` wystąpienie.</span><span class="sxs-lookup"><span data-stu-id="8bc95-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="8bc95-104">Certyfikat może zostać wystawiony przez prywatny urząd certyfikacji i zainstalowany w usłudze zarządzania interfejsami API do `CertificateAuthority` magazynu lub do `Root` magazynu.</span><span class="sxs-lookup"><span data-stu-id="8bc95-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

## <span data-ttu-id="8bc95-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8bc95-105">SYNTAX</span></span>

```
New-AzApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bc95-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="8bc95-106">DESCRIPTION</span></span>
<span data-ttu-id="8bc95-107">Polecenie cmdlet **New-AzApiManagementSystemCertificate** to polecenie pomocnika, które tworzy wystąpienie **polecenia PsApiManagementSystemCertificate.**</span><span class="sxs-lookup"><span data-stu-id="8bc95-107">The **New-AzApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="8bc95-108">To polecenie jest używane z poleceniem cmdlet New-AzApiManagement i Set-AzApiManagement cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bc95-108">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="8bc95-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8bc95-109">EXAMPLES</span></span>

### <span data-ttu-id="8bc95-110">Przykład 1. Tworzenie i inicjowanie wystąpienia pliku PsApiManagementSystemCertificate przy użyciu certyfikatu SSL z pliku</span><span class="sxs-lookup"><span data-stu-id="8bc95-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="8bc95-111">To polecenie tworzy i inicjuje wystąpienie narzędzia **PsApiManagementSystemCertificate** z certyfikatem głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="8bc95-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="8bc95-112">Następnie tworzy usługę zarządzania interfejsami API, która instaluje certyfikat certyfikacji w sklepie głównym.</span><span class="sxs-lookup"><span data-stu-id="8bc95-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="8bc95-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8bc95-113">PARAMETERS</span></span>

### <span data-ttu-id="8bc95-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bc95-114">-DefaultProfile</span></span>
<span data-ttu-id="8bc95-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8bc95-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bc95-116">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="8bc95-116">-PfxPassword</span></span>
<span data-ttu-id="8bc95-117">Hasło do pliku certyfikatu pfx.</span><span class="sxs-lookup"><span data-stu-id="8bc95-117">Password for the .pfx certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bc95-118">- PfxPath</span><span class="sxs-lookup"><span data-stu-id="8bc95-118">-PfxPath</span></span>
<span data-ttu-id="8bc95-119">Ścieżka do pliku certyfikatu pfx.</span><span class="sxs-lookup"><span data-stu-id="8bc95-119">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="8bc95-120">-StoreName</span><span class="sxs-lookup"><span data-stu-id="8bc95-120">-StoreName</span></span>
<span data-ttu-id="8bc95-121">Nazwa magazynu certyfikatów</span><span class="sxs-lookup"><span data-stu-id="8bc95-121">Certificate StoreName</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: CertificateAuthority, Root

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bc95-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bc95-122">CommonParameters</span></span>
<span data-ttu-id="8bc95-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bc95-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bc95-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8bc95-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bc95-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8bc95-125">INPUTS</span></span>

### <span data-ttu-id="8bc95-126">System.String</span><span class="sxs-lookup"><span data-stu-id="8bc95-126">System.String</span></span>

### <span data-ttu-id="8bc95-127">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="8bc95-127">System.Security.SecureString</span></span>

## <span data-ttu-id="8bc95-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8bc95-128">OUTPUTS</span></span>

### <span data-ttu-id="8bc95-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="8bc95-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="8bc95-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8bc95-130">NOTES</span></span>

## <span data-ttu-id="8bc95-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8bc95-131">RELATED LINKS</span></span>

[<span data-ttu-id="8bc95-132">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="8bc95-132">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="8bc95-133">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="8bc95-133">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)