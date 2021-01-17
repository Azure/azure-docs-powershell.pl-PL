---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
ms.openlocfilehash: ec64a339c29facdbb940b8141c72222ff932c1bd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330982"
---
# <span data-ttu-id="b8bb2-101">Get-AzApiManagementTenantAccessSecret</span><span class="sxs-lookup"><span data-stu-id="b8bb2-101">Get-AzApiManagementTenantAccessSecret</span></span>

## <span data-ttu-id="b8bb2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b8bb2-102">SYNOPSIS</span></span>
<span data-ttu-id="b8bb2-103">Pobiera klucze konfiguracji programu Access dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="b8bb2-103">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="b8bb2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b8bb2-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8bb2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b8bb2-105">DESCRIPTION</span></span>
<span data-ttu-id="b8bb2-106">Pobiera klucze konfiguracji programu Access dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="b8bb2-106">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="b8bb2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b8bb2-107">EXAMPLES</span></span>

### <span data-ttu-id="b8bb2-108">Przykład 1: Uzyskaj klucze konfiguracji dostępu do dzierżawy</span><span class="sxs-lookup"><span data-stu-id="b8bb2-108">Example 1: Get tenant access configuration keys</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccessSecret -Context $apimContext
```

<span data-ttu-id="b8bb2-109">To polecenie pobiera klucze konfiguracji dostępu do dzierżawy dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="b8bb2-109">This command gets the tenant access configuration keys for the specified context.</span></span>

## <span data-ttu-id="b8bb2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b8bb2-110">PARAMETERS</span></span>

### <span data-ttu-id="b8bb2-111">-Context</span><span class="sxs-lookup"><span data-stu-id="b8bb2-111">-Context</span></span>
<span data-ttu-id="b8bb2-112">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b8bb2-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b8bb2-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b8bb2-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8bb2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8bb2-114">-DefaultProfile</span></span>
<span data-ttu-id="b8bb2-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b8bb2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8bb2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8bb2-116">CommonParameters</span></span>
<span data-ttu-id="b8bb2-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8bb2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8bb2-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8bb2-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8bb2-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8bb2-119">INPUTS</span></span>

### <span data-ttu-id="b8bb2-120">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b8bb2-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="b8bb2-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b8bb2-121">OUTPUTS</span></span>

### <span data-ttu-id="b8bb2-122">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="b8bb2-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="b8bb2-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b8bb2-123">NOTES</span></span>

## <span data-ttu-id="b8bb2-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8bb2-124">RELATED LINKS</span></span>
