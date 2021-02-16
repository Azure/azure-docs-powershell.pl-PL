---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: ea18df702913cd2ec7404a3fccb110f85e12ee47
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244435"
---
# <span data-ttu-id="52154-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="52154-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="52154-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52154-102">SYNOPSIS</span></span>
<span data-ttu-id="52154-103">Tworzy wystąpienie zestawu PsApiManagementSslSetting.</span><span class="sxs-lookup"><span data-stu-id="52154-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="52154-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="52154-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52154-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="52154-105">DESCRIPTION</span></span>
<span data-ttu-id="52154-106">Polecenie Pomocnik służące do tworzenia wystąpienia polecenia PsApiManagementSslSetting.</span><span class="sxs-lookup"><span data-stu-id="52154-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="52154-107">To polecenie ma być używane razem z New-AzApiManagement polecenia.</span><span class="sxs-lookup"><span data-stu-id="52154-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="52154-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="52154-108">EXAMPLES</span></span>

### <span data-ttu-id="52154-109">Przykład 1. Tworzenie ustawienia protokołu SSL w celu włączenia protokołu TLS 1.0 zarówno w przypadku zaplecza, jak i frontendu</span><span class="sxs-lookup"><span data-stu-id="52154-109">Example 1: Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="52154-110">Utwórz nowe wystąpienie funkcji PsApiManagementSslSetting, aby włączyć funkcję TLSv 1.0 zarówno w interfejsie Frontend (między klientem a interfejsem APIM), jak i w zaplecza (między interfejsem APIM i zaplecza) bramy ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="52154-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="52154-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52154-111">PARAMETERS</span></span>

### <span data-ttu-id="52154-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="52154-112">-BackendProtocol</span></span>
<span data-ttu-id="52154-113">Ustawienia protokołu zabezpieczeń wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="52154-113">Backend Security protocol settings.</span></span> <span data-ttu-id="52154-114">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="52154-114">This parameter is optional.</span></span>
<span data-ttu-id="52154-115">Prawidłowe ustawienia protokołu `Tls11` to: Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="52154-115">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>

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

### <span data-ttu-id="52154-116">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="52154-116">-CipherSuite</span></span>
<span data-ttu-id="52154-117">Ustawienia pakietów szyfrowania ssl w określonej kolejności.</span><span class="sxs-lookup"><span data-stu-id="52154-117">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="52154-118">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="52154-118">This parameter is optional.</span></span>
<span data-ttu-id="52154-119">Prawidłowe ustawienia `TripleDes168` to: Włącz/Wyłącz Tripe Des 168</span><span class="sxs-lookup"><span data-stu-id="52154-119">The valid Settings are `TripleDes168` - Enable / Disable Tripe Des 168</span></span>

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

### <span data-ttu-id="52154-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52154-120">-DefaultProfile</span></span>
<span data-ttu-id="52154-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="52154-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52154-122">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="52154-122">-FrontendProtocol</span></span>
<span data-ttu-id="52154-123">Ustawienia protokołów zabezpieczeń frontend.</span><span class="sxs-lookup"><span data-stu-id="52154-123">Frontend Security protocols settings.</span></span> <span data-ttu-id="52154-124">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="52154-124">This parameter is optional.</span></span>
<span data-ttu-id="52154-125">Prawidłowe ustawienia protokołu `Tls11` to: Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="52154-125">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>


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

### <span data-ttu-id="52154-126">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="52154-126">-ServerProtocol</span></span>
<span data-ttu-id="52154-127">Ustawienia protokołu serwera, takie jak Http2.</span><span class="sxs-lookup"><span data-stu-id="52154-127">Server protocol settings like Http2.</span></span> <span data-ttu-id="52154-128">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="52154-128">This parameter is optional.</span></span>
<span data-ttu-id="52154-129">Prawidłowe ustawienia `Http2` to: Włącz http 2.0</span><span class="sxs-lookup"><span data-stu-id="52154-129">The valid Settings are `Http2` - Enable Http 2.0</span></span>

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

### <span data-ttu-id="52154-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52154-130">CommonParameters</span></span>
<span data-ttu-id="52154-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52154-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52154-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52154-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52154-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52154-133">INPUTS</span></span>

### <span data-ttu-id="52154-134">Brak</span><span class="sxs-lookup"><span data-stu-id="52154-134">None</span></span>

## <span data-ttu-id="52154-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52154-135">OUTPUTS</span></span>

### <span data-ttu-id="52154-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="52154-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="52154-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="52154-137">NOTES</span></span>

## <span data-ttu-id="52154-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52154-138">RELATED LINKS</span></span>

[<span data-ttu-id="52154-139">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="52154-139">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

