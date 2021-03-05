---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
ms.openlocfilehash: 841be3a5bba812538e55fa3bd74b4bc9878aff13
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960922"
---
# <span data-ttu-id="b0982-101">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="b0982-101">New-AzApiManagementBackendProxy</span></span>

## <span data-ttu-id="b0982-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0982-102">SYNOPSIS</span></span>
<span data-ttu-id="b0982-103">Tworzy nowy obiekt serwera proxy zaplecza.</span><span class="sxs-lookup"><span data-stu-id="b0982-103">Creates a new Backend Proxy Object.</span></span>

## <span data-ttu-id="b0982-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b0982-104">SYNTAX</span></span>

```
New-AzApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0982-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b0982-105">DESCRIPTION</span></span>
<span data-ttu-id="b0982-106">Tworzy nowy obiekt serwera proxy zaplecza, który można tworzyć potokami podczas tworzenia nowej jednostki zaplecza.</span><span class="sxs-lookup"><span data-stu-id="b0982-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="b0982-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b0982-107">EXAMPLES</span></span>

### <span data-ttu-id="b0982-108">Przykład 1. Tworzenie obiektu proxy zaplecza In-Memory serwera proxy</span><span class="sxs-lookup"><span data-stu-id="b0982-108">Example 1: Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="b0982-109">Tworzy obiekt serwera proxy zaplecza i konfiguruje zaplecza</span><span class="sxs-lookup"><span data-stu-id="b0982-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="b0982-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0982-110">PARAMETERS</span></span>

### <span data-ttu-id="b0982-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0982-111">-DefaultProfile</span></span>
<span data-ttu-id="b0982-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0982-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0982-113">- ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="b0982-113">-ProxyCredential</span></span>
<span data-ttu-id="b0982-114">Poświadczenia używane do łączenia się z serwerem proxy zaplecza.</span><span class="sxs-lookup"><span data-stu-id="b0982-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="b0982-115">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b0982-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="b0982-116">— adres URL</span><span class="sxs-lookup"><span data-stu-id="b0982-116">-Url</span></span>
<span data-ttu-id="b0982-117">Adres URL serwera proxy używanego podczas przekazywania połączeń do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="b0982-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="b0982-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b0982-118">This parameter is required.</span></span>

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

### <span data-ttu-id="b0982-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0982-119">CommonParameters</span></span>
<span data-ttu-id="b0982-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0982-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0982-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0982-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0982-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0982-122">INPUTS</span></span>

### <span data-ttu-id="b0982-123">Brak</span><span class="sxs-lookup"><span data-stu-id="b0982-123">None</span></span>

## <span data-ttu-id="b0982-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0982-124">OUTPUTS</span></span>

### <span data-ttu-id="b0982-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="b0982-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="b0982-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b0982-126">NOTES</span></span>

## <span data-ttu-id="b0982-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0982-127">RELATED LINKS</span></span>

[<span data-ttu-id="b0982-128">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b0982-128">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="b0982-129">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b0982-129">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="b0982-130">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="b0982-130">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="b0982-131">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b0982-131">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="b0982-132">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b0982-132">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
