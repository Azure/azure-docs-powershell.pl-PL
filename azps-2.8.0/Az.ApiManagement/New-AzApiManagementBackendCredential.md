---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: ded8b44940c227477f6ad3dfdd7d4b673161fca1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399451"
---
# <span data-ttu-id="ea133-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="ea133-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="ea133-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea133-102">SYNOPSIS</span></span>
<span data-ttu-id="ea133-103">Tworzy nową umowę poświadczeń zaplecza.</span><span class="sxs-lookup"><span data-stu-id="ea133-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="ea133-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ea133-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea133-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ea133-105">DESCRIPTION</span></span>
<span data-ttu-id="ea133-106">Tworzy nową umowę poświadczeń zaplecza.</span><span class="sxs-lookup"><span data-stu-id="ea133-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="ea133-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ea133-107">EXAMPLES</span></span>

### <span data-ttu-id="ea133-108">Tworzenie poświadczeń zaplecza dla In-Memory danych</span><span class="sxs-lookup"><span data-stu-id="ea133-108">Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="ea133-109">Tworzy umowę poświadczeń zaplecza</span><span class="sxs-lookup"><span data-stu-id="ea133-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="ea133-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea133-110">PARAMETERS</span></span>

### <span data-ttu-id="ea133-111">-AuthorizationHeaderParameters</span><span class="sxs-lookup"><span data-stu-id="ea133-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="ea133-112">Nagłówek autoryzacji używany dla zaplecza.</span><span class="sxs-lookup"><span data-stu-id="ea133-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="ea133-113">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ea133-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="ea133-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="ea133-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="ea133-115">Schemat autoryzacji używany dla zaplecza.</span><span class="sxs-lookup"><span data-stu-id="ea133-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="ea133-116">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ea133-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="ea133-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="ea133-117">-CertificateThumbprint</span></span>
<span data-ttu-id="ea133-118">Thumbprints certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="ea133-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="ea133-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ea133-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="ea133-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea133-120">-DefaultProfile</span></span>
<span data-ttu-id="ea133-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea133-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea133-122">— Nagłówek</span><span class="sxs-lookup"><span data-stu-id="ea133-122">-Header</span></span>
<span data-ttu-id="ea133-123">Wartości parametrów nagłówka zaakceptowane przez zaplecza.</span><span class="sxs-lookup"><span data-stu-id="ea133-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="ea133-124">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ea133-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="ea133-125">— zapytanie</span><span class="sxs-lookup"><span data-stu-id="ea133-125">-Query</span></span>
<span data-ttu-id="ea133-126">Wartości parametrów kwerendy zaakceptowane przez zaplecza.</span><span class="sxs-lookup"><span data-stu-id="ea133-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="ea133-127">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ea133-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="ea133-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea133-128">CommonParameters</span></span>
<span data-ttu-id="ea133-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea133-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea133-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea133-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea133-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea133-131">INPUTS</span></span>

### <span data-ttu-id="ea133-132">Brak</span><span class="sxs-lookup"><span data-stu-id="ea133-132">None</span></span>

## <span data-ttu-id="ea133-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea133-133">OUTPUTS</span></span>

### <span data-ttu-id="ea133-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="ea133-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="ea133-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ea133-135">NOTES</span></span>

## <span data-ttu-id="ea133-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea133-136">RELATED LINKS</span></span>

[<span data-ttu-id="ea133-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ea133-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="ea133-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ea133-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="ea133-139">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="ea133-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="ea133-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ea133-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="ea133-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ea133-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
