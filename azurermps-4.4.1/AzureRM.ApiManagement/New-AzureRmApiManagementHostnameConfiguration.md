---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D4C465CE-1B8A-4CFC-BAA8-21CC66B7D6D6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
ms.openlocfilehash: 1b34903f402f7e8d432d16087f1e32fc7b7da3e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547204"
---
# <span data-ttu-id="8294d-101">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="8294d-101">New-AzureRmApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="8294d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8294d-102">SYNOPSIS</span></span>
<span data-ttu-id="8294d-103">Tworzy wystąpienie PsApiManagementHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8294d-103">Creates an instance of PsApiManagementHostnameConfiguration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8294d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8294d-104">SYNTAX</span></span>

```
New-AzureRmApiManagementHostnameConfiguration -CertificateThumbprint <String> -Hostname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8294d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8294d-105">DESCRIPTION</span></span>
<span data-ttu-id="8294d-106">Polecenie cmdlet **New-AzureRmApiManagementHostnameConfiguration** jest poleceniem pomagającym, które tworzy wystąpienie **PsApiManagementHostnameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="8294d-106">The **New-AzureRmApiManagementHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementHostnameConfiguration**.</span></span>
<span data-ttu-id="8294d-107">To polecenie jest używane w przypadku polecenia cmdlet Set-AzureRmApiManagementHostnames.</span><span class="sxs-lookup"><span data-stu-id="8294d-107">This command is used with the Set-AzureRmApiManagementHostnames cmdlet.</span></span>

## <span data-ttu-id="8294d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8294d-108">EXAMPLES</span></span>

### <span data-ttu-id="8294d-109">Przykład 1. Tworzenie i Inicjowanie wystąpienia PsApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="8294d-109">Example 1: Create and initialize an instance of PsApiManagementHostnameConfiguration</span></span>
```
PS C:\>New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
```

<span data-ttu-id="8294d-110">To polecenie tworzy i Inicjuje wystąpienie **PsApiManagementHostnameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="8294d-110">This command creates and initializes an instance of **PsApiManagementHostnameConfiguration**.</span></span>

## <span data-ttu-id="8294d-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8294d-111">PARAMETERS</span></span>

### <span data-ttu-id="8294d-112">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="8294d-112">-CertificateThumbprint</span></span>
<span data-ttu-id="8294d-113">Określa odcisk palca certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="8294d-113">Specifies the certificate thumbprint.</span></span>
<span data-ttu-id="8294d-114">Certyfikat należy najpierw zaimportować za pomocą polecenia cmdlet Import-AzureRmApiManagementHostnameCertificate.</span><span class="sxs-lookup"><span data-stu-id="8294d-114">The certificate must be first imported with the Import-AzureRmApiManagementHostnameCertificate cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8294d-115">-Hostname</span><span class="sxs-lookup"><span data-stu-id="8294d-115">-Hostname</span></span>
<span data-ttu-id="8294d-116">Określa niestandardową nazwę hosta, dla którego to polecenie cmdlet tworzy wystąpienie **PsApiManagementHostnameConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="8294d-116">Specifies the custom host name for which this cmdlet creates the **PsApiManagementHostnameConfiguration** instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8294d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8294d-117">-DefaultProfile</span></span>
<span data-ttu-id="8294d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8294d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8294d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8294d-119">CommonParameters</span></span>
<span data-ttu-id="8294d-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8294d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8294d-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8294d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8294d-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8294d-122">INPUTS</span></span>

## <span data-ttu-id="8294d-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8294d-123">OUTPUTS</span></span>

### <span data-ttu-id="8294d-124">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="8294d-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="8294d-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8294d-125">NOTES</span></span>

## <span data-ttu-id="8294d-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8294d-126">RELATED LINKS</span></span>

[<span data-ttu-id="8294d-127">Import — AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="8294d-127">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="8294d-128">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="8294d-128">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)


