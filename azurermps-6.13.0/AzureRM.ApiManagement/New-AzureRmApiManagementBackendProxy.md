---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
ms.openlocfilehash: d5ff2fd4f9bd3360974d93c457e541cb2f96dc5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542040"
---
# <span data-ttu-id="cade2-101">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="cade2-101">New-AzureRmApiManagementBackendProxy</span></span>

## <span data-ttu-id="cade2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cade2-102">SYNOPSIS</span></span>
<span data-ttu-id="cade2-103">Tworzy nowy obiekt pośredniczący zaplecza.</span><span class="sxs-lookup"><span data-stu-id="cade2-103">Creates a new Backend Proxy Object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cade2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cade2-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cade2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cade2-105">DESCRIPTION</span></span>
<span data-ttu-id="cade2-106">Tworzy nowy obiekt pośredniczący zaplecza, który może zostać potokiem podczas tworzenia nowej jednostki wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="cade2-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="cade2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cade2-107">EXAMPLES</span></span>

### <span data-ttu-id="cade2-108">Tworzenie obiektu pośredniczącego w wewnętrznej bazie danych In-Memory</span><span class="sxs-lookup"><span data-stu-id="cade2-108">Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzureRmApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="cade2-109">Tworzy obiekt pośredniczący zaplecza i konfiguruje zaplecze</span><span class="sxs-lookup"><span data-stu-id="cade2-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="cade2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cade2-110">PARAMETERS</span></span>

### <span data-ttu-id="cade2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cade2-111">-DefaultProfile</span></span>
<span data-ttu-id="cade2-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cade2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cade2-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="cade2-113">-ProxyCredential</span></span>
<span data-ttu-id="cade2-114">Poświadczenia służące do nawiązywania połączenia z serwerem proxy zaplecza.</span><span class="sxs-lookup"><span data-stu-id="cade2-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="cade2-115">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="cade2-115">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cade2-116">-URL</span><span class="sxs-lookup"><span data-stu-id="cade2-116">-Url</span></span>
<span data-ttu-id="cade2-117">Adres URL serwera proxy, który ma być używany podczas przekierowywania połączeń do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="cade2-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="cade2-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="cade2-118">This parameter is required.</span></span>

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

### <span data-ttu-id="cade2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cade2-119">CommonParameters</span></span>
<span data-ttu-id="cade2-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cade2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cade2-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cade2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cade2-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cade2-122">INPUTS</span></span>

### <span data-ttu-id="cade2-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="cade2-123">None</span></span>

## <span data-ttu-id="cade2-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cade2-124">OUTPUTS</span></span>

### <span data-ttu-id="cade2-125">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="cade2-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="cade2-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cade2-126">NOTES</span></span>

## <span data-ttu-id="cade2-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cade2-127">RELATED LINKS</span></span>

[<span data-ttu-id="cade2-128">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cade2-128">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="cade2-129">Nowe — AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cade2-129">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="cade2-130">Nowe — AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="cade2-130">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="cade2-131">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cade2-131">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="cade2-132">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cade2-132">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
