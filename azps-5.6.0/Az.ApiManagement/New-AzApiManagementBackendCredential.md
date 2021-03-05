---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: 0d865e2b9e1459f326367a499e30bc37467628cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966858"
---
# <span data-ttu-id="6545a-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="6545a-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="6545a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6545a-102">SYNOPSIS</span></span>
<span data-ttu-id="6545a-103">Tworzy nową umowę poświadczeń zaplecza.</span><span class="sxs-lookup"><span data-stu-id="6545a-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="6545a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6545a-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6545a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6545a-105">DESCRIPTION</span></span>
<span data-ttu-id="6545a-106">Tworzy nową umowę poświadczeń zaplecza.</span><span class="sxs-lookup"><span data-stu-id="6545a-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="6545a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6545a-107">EXAMPLES</span></span>

### <span data-ttu-id="6545a-108">Przykład 1. Tworzenie poświadczeń zaplecza dla In-Memory obiektu</span><span class="sxs-lookup"><span data-stu-id="6545a-108">Example 1: Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="6545a-109">Tworzy umowę poświadczeń zaplecza</span><span class="sxs-lookup"><span data-stu-id="6545a-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="6545a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6545a-110">PARAMETERS</span></span>

### <span data-ttu-id="6545a-111">-AuthorizationHeaderParameters</span><span class="sxs-lookup"><span data-stu-id="6545a-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="6545a-112">Nagłówek autoryzacji używany dla zaplecza.</span><span class="sxs-lookup"><span data-stu-id="6545a-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="6545a-113">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="6545a-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6545a-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="6545a-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="6545a-115">Schemat autoryzacji używany dla zaplecza.</span><span class="sxs-lookup"><span data-stu-id="6545a-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="6545a-116">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="6545a-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6545a-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="6545a-117">-CertificateThumbprint</span></span>
<span data-ttu-id="6545a-118">Thumbprints certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="6545a-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="6545a-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="6545a-119">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6545a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6545a-120">-DefaultProfile</span></span>
<span data-ttu-id="6545a-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6545a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6545a-122">— Nagłówek</span><span class="sxs-lookup"><span data-stu-id="6545a-122">-Header</span></span>
<span data-ttu-id="6545a-123">Wartości parametrów nagłówka zaakceptowane przez zaplecza.</span><span class="sxs-lookup"><span data-stu-id="6545a-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="6545a-124">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="6545a-124">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6545a-125">— zapytanie</span><span class="sxs-lookup"><span data-stu-id="6545a-125">-Query</span></span>
<span data-ttu-id="6545a-126">Wartości parametrów kwerendy zaakceptowane przez zaplecza.</span><span class="sxs-lookup"><span data-stu-id="6545a-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="6545a-127">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="6545a-127">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6545a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6545a-128">CommonParameters</span></span>
<span data-ttu-id="6545a-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6545a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6545a-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6545a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6545a-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6545a-131">INPUTS</span></span>

### <span data-ttu-id="6545a-132">Brak</span><span class="sxs-lookup"><span data-stu-id="6545a-132">None</span></span>

## <span data-ttu-id="6545a-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6545a-133">OUTPUTS</span></span>

### <span data-ttu-id="6545a-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="6545a-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="6545a-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6545a-135">NOTES</span></span>

## <span data-ttu-id="6545a-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6545a-136">RELATED LINKS</span></span>

[<span data-ttu-id="6545a-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6545a-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="6545a-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6545a-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="6545a-139">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="6545a-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="6545a-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6545a-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="6545a-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6545a-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
