---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: 2418ec3f5e9570046c37c76bdaef8f853ff819b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704631"
---
# <span data-ttu-id="7588f-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="7588f-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="7588f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7588f-102">SYNOPSIS</span></span>
<span data-ttu-id="7588f-103">Pobiera konfigurację dostępu dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="7588f-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="7588f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7588f-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7588f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7588f-105">DESCRIPTION</span></span>
<span data-ttu-id="7588f-106">Polecenie cmdlet **Get-AzApiManagementTenantAccess** Pobiera konfigurację dostępu dzierżawy dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="7588f-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="7588f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7588f-107">EXAMPLES</span></span>

### <span data-ttu-id="7588f-108">Przykład 1: Pobieranie konfiguracji dostępu dzierżawy</span><span class="sxs-lookup"><span data-stu-id="7588f-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="7588f-109">To polecenie pobiera konfigurację dostępu dzierżawy dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="7588f-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="7588f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7588f-110">PARAMETERS</span></span>

### <span data-ttu-id="7588f-111">-Context</span><span class="sxs-lookup"><span data-stu-id="7588f-111">-Context</span></span>
<span data-ttu-id="7588f-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="7588f-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7588f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7588f-113">-DefaultProfile</span></span>
<span data-ttu-id="7588f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7588f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7588f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7588f-115">CommonParameters</span></span>
<span data-ttu-id="7588f-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7588f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7588f-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7588f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7588f-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7588f-118">INPUTS</span></span>

### <span data-ttu-id="7588f-119">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7588f-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="7588f-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7588f-120">OUTPUTS</span></span>

### <span data-ttu-id="7588f-121">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="7588f-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="7588f-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7588f-122">NOTES</span></span>

## <span data-ttu-id="7588f-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7588f-123">RELATED LINKS</span></span>

[<span data-ttu-id="7588f-124">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="7588f-124">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


