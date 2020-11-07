---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
ms.openlocfilehash: 834a713e5fb7cc6bfcf24244bbb376eb0f01a8de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706986"
---
# <span data-ttu-id="0a996-101">New-AzApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="0a996-101">New-AzApiManagementSystemCertificate</span></span>

## <span data-ttu-id="0a996-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0a996-102">SYNOPSIS</span></span>
<span data-ttu-id="0a996-103">Tworzy wystąpienie `PsApiManagementSystemCertificate` .</span><span class="sxs-lookup"><span data-stu-id="0a996-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="0a996-104">Certyfikat może zostać wystawiony przez prywatny urząd certyfikacji i zostanie zainstalowany w usłudze zarządzania interfejsem API `CertificateAuthority` lub w `Root` sklepie.</span><span class="sxs-lookup"><span data-stu-id="0a996-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

## <span data-ttu-id="0a996-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0a996-105">SYNTAX</span></span>

```
New-AzApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a996-106">Opis</span><span class="sxs-lookup"><span data-stu-id="0a996-106">DESCRIPTION</span></span>
<span data-ttu-id="0a996-107">Polecenie cmdlet **New-AzApiManagementSystemCertificate** jest poleceniem pomagającym, które tworzy wystąpienie **PsApiManagementSystemCertificate**.</span><span class="sxs-lookup"><span data-stu-id="0a996-107">The **New-AzApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="0a996-108">To polecenie jest używane w przypadku polecenia cmdlet New-AzApiManagement i Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="0a996-108">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="0a996-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0a996-109">EXAMPLES</span></span>

### <span data-ttu-id="0a996-110">Przykład 1: Tworzenie i Inicjowanie wystąpienia PsApiManagementSystemCertificate przy użyciu certyfikatu SSL z pliku</span><span class="sxs-lookup"><span data-stu-id="0a996-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="0a996-111">To polecenie tworzy i Inicjuje wystąpienie **PsApiManagementSystemCertificate** przy użyciu certyfikatu głównego urzędu certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="0a996-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="0a996-112">Następnie tworzy i usługa zarządzania interfejsem API, która instaluje certyfikat urzędu certyfikacji w magazynie głównym.</span><span class="sxs-lookup"><span data-stu-id="0a996-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="0a996-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0a996-113">PARAMETERS</span></span>

### <span data-ttu-id="0a996-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a996-114">-DefaultProfile</span></span>
<span data-ttu-id="0a996-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0a996-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a996-116">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="0a996-116">-PfxPassword</span></span>
<span data-ttu-id="0a996-117">Hasło do pliku certyfikatu PFX.</span><span class="sxs-lookup"><span data-stu-id="0a996-117">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="0a996-118">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="0a996-118">-PfxPath</span></span>
<span data-ttu-id="0a996-119">Ścieżka do pliku certyfikatu PFX.</span><span class="sxs-lookup"><span data-stu-id="0a996-119">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="0a996-120">-Pole NazwaSklepu</span><span class="sxs-lookup"><span data-stu-id="0a996-120">-StoreName</span></span>
<span data-ttu-id="0a996-121">Certyfikat pole NazwaSklepu</span><span class="sxs-lookup"><span data-stu-id="0a996-121">Certificate StoreName</span></span>

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

### <span data-ttu-id="0a996-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a996-122">CommonParameters</span></span>
<span data-ttu-id="0a996-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a996-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a996-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a996-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a996-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a996-125">INPUTS</span></span>

### <span data-ttu-id="0a996-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0a996-126">System.String</span></span>

### <span data-ttu-id="0a996-127">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="0a996-127">System.Security.SecureString</span></span>

## <span data-ttu-id="0a996-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0a996-128">OUTPUTS</span></span>

### <span data-ttu-id="0a996-129">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="0a996-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="0a996-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0a996-130">NOTES</span></span>

## <span data-ttu-id="0a996-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a996-131">RELATED LINKS</span></span>

[<span data-ttu-id="0a996-132">Nowe — AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a996-132">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="0a996-133">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a996-133">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)