---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: ea18df702913cd2ec7404a3fccb110f85e12ee47
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222731"
---
# <span data-ttu-id="8217b-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="8217b-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="8217b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8217b-102">SYNOPSIS</span></span>
<span data-ttu-id="8217b-103">Tworzy wystąpienie PsApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="8217b-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="8217b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8217b-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8217b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8217b-105">DESCRIPTION</span></span>
<span data-ttu-id="8217b-106">Polecenie pomocnika tworzenia wystąpienia PsApiManagementSslSetting.</span><span class="sxs-lookup"><span data-stu-id="8217b-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="8217b-107">To polecenie jest używane z poleceniem New-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="8217b-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="8217b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8217b-108">EXAMPLES</span></span>

### <span data-ttu-id="8217b-109">Przykład 1: Tworzenie ustawienia SSL w celu włączenia protokołu TLS 1,0 zarówno w wewnętrznej bazie danych, jak i frontonie</span><span class="sxs-lookup"><span data-stu-id="8217b-109">Example 1: Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="8217b-110">Utwórz nowe wystąpienie PsApiManagementSslSetting, aby włączyć TLSv 1,0 zarówno na frontonie (między klientem a APIM), jak i zaplecza (między APIM i zapleczem) bramy ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="8217b-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="8217b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8217b-111">PARAMETERS</span></span>

### <span data-ttu-id="8217b-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="8217b-112">-BackendProtocol</span></span>
<span data-ttu-id="8217b-113">Ustawienia protokołu zabezpieczeń zaplecza.</span><span class="sxs-lookup"><span data-stu-id="8217b-113">Backend Security protocol settings.</span></span> <span data-ttu-id="8217b-114">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="8217b-114">This parameter is optional.</span></span>
<span data-ttu-id="8217b-115">Prawidłowe ustawienia protokołu to `Tls11` tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0</span><span class="sxs-lookup"><span data-stu-id="8217b-115">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>

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

### <span data-ttu-id="8217b-116">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="8217b-116">-CipherSuite</span></span>
<span data-ttu-id="8217b-117">Ustawienia mechanizmów szyfrowania SSL w określonej kolejności.</span><span class="sxs-lookup"><span data-stu-id="8217b-117">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="8217b-118">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="8217b-118">This parameter is optional.</span></span>
<span data-ttu-id="8217b-119">Prawidłowe ustawienia to `TripleDes168` Włączanie/wyłączanie wyjazdu Des 168</span><span class="sxs-lookup"><span data-stu-id="8217b-119">The valid Settings are `TripleDes168` - Enable / Disable Tripe Des 168</span></span>

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

### <span data-ttu-id="8217b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8217b-120">-DefaultProfile</span></span>
<span data-ttu-id="8217b-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8217b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8217b-122">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="8217b-122">-FrontendProtocol</span></span>
<span data-ttu-id="8217b-123">Ustawienia protokołów zabezpieczeń frontonu.</span><span class="sxs-lookup"><span data-stu-id="8217b-123">Frontend Security protocols settings.</span></span> <span data-ttu-id="8217b-124">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="8217b-124">This parameter is optional.</span></span>
<span data-ttu-id="8217b-125">Prawidłowe ustawienia protokołu to `Tls11` tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0</span><span class="sxs-lookup"><span data-stu-id="8217b-125">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>


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

### <span data-ttu-id="8217b-126">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="8217b-126">-ServerProtocol</span></span>
<span data-ttu-id="8217b-127">Ustawienia protokołu serwera, takie jak Http2.</span><span class="sxs-lookup"><span data-stu-id="8217b-127">Server protocol settings like Http2.</span></span> <span data-ttu-id="8217b-128">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="8217b-128">This parameter is optional.</span></span>
<span data-ttu-id="8217b-129">Prawidłowe ustawienia to `Http2` enable Http 2,0</span><span class="sxs-lookup"><span data-stu-id="8217b-129">The valid Settings are `Http2` - Enable Http 2.0</span></span>

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

### <span data-ttu-id="8217b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8217b-130">CommonParameters</span></span>
<span data-ttu-id="8217b-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8217b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8217b-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8217b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8217b-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8217b-133">INPUTS</span></span>

### <span data-ttu-id="8217b-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8217b-134">None</span></span>

## <span data-ttu-id="8217b-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8217b-135">OUTPUTS</span></span>

### <span data-ttu-id="8217b-136">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="8217b-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="8217b-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8217b-137">NOTES</span></span>

## <span data-ttu-id="8217b-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8217b-138">RELATED LINKS</span></span>

[<span data-ttu-id="8217b-139">Nowe — AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="8217b-139">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

