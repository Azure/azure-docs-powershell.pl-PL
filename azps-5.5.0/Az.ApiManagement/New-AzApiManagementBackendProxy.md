---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
ms.openlocfilehash: fe4d94bb438d3180ed0a77bb7129b46c65d5edbc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239754"
---
# <span data-ttu-id="d646f-101">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="d646f-101">New-AzApiManagementBackendProxy</span></span>

## <span data-ttu-id="d646f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d646f-102">SYNOPSIS</span></span>
<span data-ttu-id="d646f-103">Tworzy nowy obiekt serwera proxy zaplecza.</span><span class="sxs-lookup"><span data-stu-id="d646f-103">Creates a new Backend Proxy Object.</span></span>

## <span data-ttu-id="d646f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d646f-104">SYNTAX</span></span>

```
New-AzApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d646f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d646f-105">DESCRIPTION</span></span>
<span data-ttu-id="d646f-106">Tworzy nowy obiekt serwera proxy zaplecza, który można tworzyć potokami podczas tworzenia nowej jednostki zaplecza.</span><span class="sxs-lookup"><span data-stu-id="d646f-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="d646f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d646f-107">EXAMPLES</span></span>

### <span data-ttu-id="d646f-108">Przykład 1. Tworzenie serwera proxy zaplecza In-Memory serwera proxy</span><span class="sxs-lookup"><span data-stu-id="d646f-108">Example 1: Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="d646f-109">Tworzy obiekt serwera proxy zaplecza i konfiguruje zaplecza</span><span class="sxs-lookup"><span data-stu-id="d646f-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="d646f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d646f-110">PARAMETERS</span></span>

### <span data-ttu-id="d646f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d646f-111">-DefaultProfile</span></span>
<span data-ttu-id="d646f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d646f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d646f-113">- ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="d646f-113">-ProxyCredential</span></span>
<span data-ttu-id="d646f-114">Poświadczenia używane do łączenia się z serwerem proxy zaplecza.</span><span class="sxs-lookup"><span data-stu-id="d646f-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="d646f-115">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d646f-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="d646f-116">— adres URL</span><span class="sxs-lookup"><span data-stu-id="d646f-116">-Url</span></span>
<span data-ttu-id="d646f-117">Adres URL serwera proxy używanego podczas przekazywania połączeń do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="d646f-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="d646f-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d646f-118">This parameter is required.</span></span>

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

### <span data-ttu-id="d646f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d646f-119">CommonParameters</span></span>
<span data-ttu-id="d646f-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d646f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d646f-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d646f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d646f-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d646f-122">INPUTS</span></span>

### <span data-ttu-id="d646f-123">Brak</span><span class="sxs-lookup"><span data-stu-id="d646f-123">None</span></span>

## <span data-ttu-id="d646f-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d646f-124">OUTPUTS</span></span>

### <span data-ttu-id="d646f-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="d646f-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="d646f-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d646f-126">NOTES</span></span>

## <span data-ttu-id="d646f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d646f-127">RELATED LINKS</span></span>

[<span data-ttu-id="d646f-128">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d646f-128">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="d646f-129">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d646f-129">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="d646f-130">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="d646f-130">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="d646f-131">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d646f-131">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="d646f-132">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d646f-132">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
