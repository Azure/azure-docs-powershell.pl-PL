---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSystemCertificate.md
ms.openlocfilehash: fa64e9bade3a6cd8ec4edc8e04956c97306328ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524730"
---
# <span data-ttu-id="7f18c-101">New-AzureRmApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="7f18c-101">New-AzureRmApiManagementSystemCertificate</span></span>

## <span data-ttu-id="7f18c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f18c-102">SYNOPSIS</span></span>
<span data-ttu-id="7f18c-103">Tworzy wystąpienie `PsApiManagementSystemCertificate` .</span><span class="sxs-lookup"><span data-stu-id="7f18c-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="7f18c-104">Certyfikat może zostać wystawiony przez prywatny urząd certyfikacji i zostanie zainstalowany w usłudze zarządzania interfejsem API `CertificateAuthority` lub w `Root` sklepie.</span><span class="sxs-lookup"><span data-stu-id="7f18c-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f18c-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f18c-105">SYNTAX</span></span>

```
New-AzureRmApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f18c-106">Opis</span><span class="sxs-lookup"><span data-stu-id="7f18c-106">DESCRIPTION</span></span>
<span data-ttu-id="7f18c-107">Polecenie cmdlet **New-AzureRmApiManagementSystemCertificate** jest poleceniem pomagającym, które tworzy wystąpienie **PsApiManagementSystemCertificate**.</span><span class="sxs-lookup"><span data-stu-id="7f18c-107">The **New-AzureRmApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="7f18c-108">To polecenie jest używane w przypadku polecenia cmdlet New-AzureRmApiManagement i Set-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="7f18c-108">This command is used with the New-AzureRmApiManagement and Set-AzureRmApiManagement cmdlet.</span></span>

## <span data-ttu-id="7f18c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f18c-109">EXAMPLES</span></span>

### <span data-ttu-id="7f18c-110">Przykład 1: Tworzenie i Inicjowanie wystąpienia PsApiManagementSystemCertificate przy użyciu certyfikatu SSL z pliku</span><span class="sxs-lookup"><span data-stu-id="7f18c-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzureRmApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="7f18c-111">To polecenie tworzy i Inicjuje wystąpienie **PsApiManagementSystemCertificate** przy użyciu certyfikatu głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="7f18c-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="7f18c-112">Następnie tworzy i usługa zarządzania interfejsem API, która instaluje certyfikat urzędu certyfikacji w magazynie głównym.</span><span class="sxs-lookup"><span data-stu-id="7f18c-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="7f18c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f18c-113">PARAMETERS</span></span>

### <span data-ttu-id="7f18c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f18c-114">-DefaultProfile</span></span>
<span data-ttu-id="7f18c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f18c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f18c-116">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="7f18c-116">-PfxPassword</span></span>
<span data-ttu-id="7f18c-117">Hasło do pliku certyfikatu PFX.</span><span class="sxs-lookup"><span data-stu-id="7f18c-117">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="7f18c-118">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="7f18c-118">-PfxPath</span></span>
<span data-ttu-id="7f18c-119">Ścieżka do pliku certyfikatu PFX.</span><span class="sxs-lookup"><span data-stu-id="7f18c-119">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="7f18c-120">-Pole NazwaSklepu</span><span class="sxs-lookup"><span data-stu-id="7f18c-120">-StoreName</span></span>
<span data-ttu-id="7f18c-121">Certyfikat pole NazwaSklepu</span><span class="sxs-lookup"><span data-stu-id="7f18c-121">Certificate StoreName</span></span>

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

### <span data-ttu-id="7f18c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f18c-122">CommonParameters</span></span>
<span data-ttu-id="7f18c-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f18c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f18c-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f18c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f18c-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f18c-125">INPUTS</span></span>

### <span data-ttu-id="7f18c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7f18c-126">System.String</span></span>

### <span data-ttu-id="7f18c-127">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="7f18c-127">System.Security.SecureString</span></span>

## <span data-ttu-id="7f18c-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f18c-128">OUTPUTS</span></span>

### <span data-ttu-id="7f18c-129">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="7f18c-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="7f18c-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f18c-130">NOTES</span></span>

## <span data-ttu-id="7f18c-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f18c-131">RELATED LINKS</span></span>

[<span data-ttu-id="7f18c-132">Nowe — AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="7f18c-132">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="7f18c-133">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="7f18c-133">Set-AzureRmApiManagement</span></span>](./Set-AzureRmApiManagement.md)
