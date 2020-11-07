---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: 7c4fb7c2147d7daf3307c2895893198ebe805ff0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706989"
---
# <span data-ttu-id="b2820-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="b2820-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="b2820-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b2820-102">SYNOPSIS</span></span>
<span data-ttu-id="b2820-103">Tworzy wystąpienie PsApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="b2820-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="b2820-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b2820-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2820-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b2820-105">DESCRIPTION</span></span>
<span data-ttu-id="b2820-106">Polecenie pomocnika tworzenia wystąpienia PsApiManagementSslSetting.</span><span class="sxs-lookup"><span data-stu-id="b2820-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="b2820-107">To polecenie jest używane z poleceniem New-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="b2820-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="b2820-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b2820-108">EXAMPLES</span></span>

### <span data-ttu-id="b2820-109">Przykład 1: Tworzenie ustawienia SSL w celu włączenia protokołu TLS 1,0 zarówno w wewnętrznej bazie danych, jak i frontonie</span><span class="sxs-lookup"><span data-stu-id="b2820-109">Example 1 : Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="b2820-110">Utwórz nowe wystąpienie PsApiManagementSslSetting, aby włączyć TLSv 1,0 zarówno na frontonie (między klientem a APIM), jak i zaplecza (między APIM i zapleczem) bramy ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="b2820-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="b2820-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b2820-111">PARAMETERS</span></span>

### <span data-ttu-id="b2820-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="b2820-112">-BackendProtocol</span></span>
<span data-ttu-id="b2820-113">Ustawienia protokołu zabezpieczeń zaplecza.</span><span class="sxs-lookup"><span data-stu-id="b2820-113">Backend Security protocol settings.</span></span> <span data-ttu-id="b2820-114">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b2820-114">This parameter is optional.</span></span>

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

### <span data-ttu-id="b2820-115">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="b2820-115">-CipherSuite</span></span>
<span data-ttu-id="b2820-116">Ustawienia mechanizmów szyfrowania SSL w określonej kolejności.</span><span class="sxs-lookup"><span data-stu-id="b2820-116">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="b2820-117">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b2820-117">This parameter is optional.</span></span>

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

### <span data-ttu-id="b2820-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2820-118">-DefaultProfile</span></span>
<span data-ttu-id="b2820-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b2820-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2820-120">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="b2820-120">-FrontendProtocol</span></span>
<span data-ttu-id="b2820-121">Ustawienia protokołów zabezpieczeń frontonu.</span><span class="sxs-lookup"><span data-stu-id="b2820-121">Frontend Security protocols settings.</span></span> <span data-ttu-id="b2820-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b2820-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="b2820-123">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="b2820-123">-ServerProtocol</span></span>
<span data-ttu-id="b2820-124">Ustawienia protokołu serwera, takie jak Http2.</span><span class="sxs-lookup"><span data-stu-id="b2820-124">Server protocol settings like Http2.</span></span> <span data-ttu-id="b2820-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b2820-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="b2820-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2820-126">CommonParameters</span></span>
<span data-ttu-id="b2820-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2820-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2820-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2820-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2820-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2820-129">INPUTS</span></span>

### <span data-ttu-id="b2820-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b2820-130">None</span></span>

## <span data-ttu-id="b2820-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b2820-131">OUTPUTS</span></span>

### <span data-ttu-id="b2820-132">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="b2820-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="b2820-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b2820-133">NOTES</span></span>

## <span data-ttu-id="b2820-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2820-134">RELATED LINKS</span></span>

[<span data-ttu-id="b2820-135">Nowe — AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b2820-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

