---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
ms.openlocfilehash: 2ce3863a546af0f8c9da3c37a75b540d2a859da1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707026"
---
# <span data-ttu-id="09d53-101">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="09d53-101">New-AzApiManagementBackendProxy</span></span>

## <span data-ttu-id="09d53-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="09d53-102">SYNOPSIS</span></span>
<span data-ttu-id="09d53-103">Tworzy nowy obiekt pośredniczący zaplecza.</span><span class="sxs-lookup"><span data-stu-id="09d53-103">Creates a new Backend Proxy Object.</span></span>

## <span data-ttu-id="09d53-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="09d53-104">SYNTAX</span></span>

```
New-AzApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09d53-105">Opis</span><span class="sxs-lookup"><span data-stu-id="09d53-105">DESCRIPTION</span></span>
<span data-ttu-id="09d53-106">Tworzy nowy obiekt pośredniczący zaplecza, który może zostać potokiem podczas tworzenia nowej jednostki wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="09d53-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="09d53-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="09d53-107">EXAMPLES</span></span>

### <span data-ttu-id="09d53-108">Tworzenie obiektu pośredniczącego w wewnętrznej bazie danych In-Memory</span><span class="sxs-lookup"><span data-stu-id="09d53-108">Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="09d53-109">Tworzy obiekt pośredniczący zaplecza i konfiguruje zaplecze</span><span class="sxs-lookup"><span data-stu-id="09d53-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="09d53-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="09d53-110">PARAMETERS</span></span>

### <span data-ttu-id="09d53-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09d53-111">-DefaultProfile</span></span>
<span data-ttu-id="09d53-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="09d53-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09d53-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="09d53-113">-ProxyCredential</span></span>
<span data-ttu-id="09d53-114">Poświadczenia służące do nawiązywania połączenia z serwerem proxy zaplecza.</span><span class="sxs-lookup"><span data-stu-id="09d53-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="09d53-115">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="09d53-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="09d53-116">-URL</span><span class="sxs-lookup"><span data-stu-id="09d53-116">-Url</span></span>
<span data-ttu-id="09d53-117">Adres URL serwera proxy, który ma być używany podczas przekierowywania połączeń do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="09d53-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="09d53-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="09d53-118">This parameter is required.</span></span>

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

### <span data-ttu-id="09d53-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09d53-119">CommonParameters</span></span>
<span data-ttu-id="09d53-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09d53-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09d53-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09d53-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09d53-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09d53-122">INPUTS</span></span>

### <span data-ttu-id="09d53-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="09d53-123">None</span></span>

## <span data-ttu-id="09d53-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="09d53-124">OUTPUTS</span></span>

### <span data-ttu-id="09d53-125">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="09d53-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="09d53-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="09d53-126">NOTES</span></span>

## <span data-ttu-id="09d53-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09d53-127">RELATED LINKS</span></span>

[<span data-ttu-id="09d53-128">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="09d53-128">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="09d53-129">Nowe — AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="09d53-129">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="09d53-130">Nowe — AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="09d53-130">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="09d53-131">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="09d53-131">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="09d53-132">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="09d53-132">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
