---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: c0c659f195aa1104b14f41e4cbc82a1ad86a1b1f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316794"
---
# <span data-ttu-id="5f5ad-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="5f5ad-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="5f5ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f5ad-102">SYNOPSIS</span></span>
<span data-ttu-id="5f5ad-103">Pobiera konfigurację dostępu dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="5f5ad-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="5f5ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f5ad-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f5ad-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5f5ad-105">DESCRIPTION</span></span>
<span data-ttu-id="5f5ad-106">Polecenie cmdlet **Get-AzApiManagementTenantAccess** Pobiera konfigurację dostępu dzierżawy dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="5f5ad-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>
<span data-ttu-id="5f5ad-107">Klucze nie zostaną uwzględnione w szczegółach wyników.</span><span class="sxs-lookup"><span data-stu-id="5f5ad-107">Keys will not be included into result details.</span></span> <span data-ttu-id="5f5ad-108">Aby uzyskać klucz tajny klienta, użyj polecenie **Get-AzApiManagementTenantAccessSecret**.</span><span class="sxs-lookup"><span data-stu-id="5f5ad-108">To get client secret, use **Get-AzApiManagementTenantAccessSecret**.</span></span>

## <span data-ttu-id="5f5ad-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f5ad-109">EXAMPLES</span></span>

### <span data-ttu-id="5f5ad-110">Przykład 1: Pobieranie konfiguracji dostępu dzierżawy</span><span class="sxs-lookup"><span data-stu-id="5f5ad-110">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="5f5ad-111">To polecenie pobiera konfigurację dostępu dzierżawy dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="5f5ad-111">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="5f5ad-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f5ad-112">PARAMETERS</span></span>

### <span data-ttu-id="5f5ad-113">-Context</span><span class="sxs-lookup"><span data-stu-id="5f5ad-113">-Context</span></span>
<span data-ttu-id="5f5ad-114">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="5f5ad-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5f5ad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f5ad-115">-DefaultProfile</span></span>
<span data-ttu-id="5f5ad-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5f5ad-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f5ad-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f5ad-117">CommonParameters</span></span>
<span data-ttu-id="5f5ad-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f5ad-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f5ad-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f5ad-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f5ad-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f5ad-120">INPUTS</span></span>

### <span data-ttu-id="5f5ad-121">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5f5ad-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="5f5ad-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f5ad-122">OUTPUTS</span></span>

### <span data-ttu-id="5f5ad-123">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="5f5ad-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="5f5ad-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f5ad-124">NOTES</span></span>

## <span data-ttu-id="5f5ad-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f5ad-125">RELATED LINKS</span></span>

[<span data-ttu-id="5f5ad-126">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="5f5ad-126">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


