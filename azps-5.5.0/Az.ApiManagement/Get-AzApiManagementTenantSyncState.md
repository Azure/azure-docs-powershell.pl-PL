---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
ms.openlocfilehash: 233c74e3939884cd4bd311ec463d81d7e7613f31
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192507"
---
# <span data-ttu-id="1265c-101">Get-AzApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="1265c-101">Get-AzApiManagementTenantSyncState</span></span>

## <span data-ttu-id="1265c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1265c-102">SYNOPSIS</span></span>
<span data-ttu-id="1265c-103">Pobiera stan ostatniej synchronizacji między bazą danych konfiguracji a repozytorium Git.</span><span class="sxs-lookup"><span data-stu-id="1265c-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="1265c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1265c-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantSyncState -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1265c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1265c-105">DESCRIPTION</span></span>
<span data-ttu-id="1265c-106">Polecenie **cmdlet Get-AzApiManagementTenantSyncState** pobiera stan ostatniej synchronizacji między bazą danych konfiguracji a repozytorium Git.</span><span class="sxs-lookup"><span data-stu-id="1265c-106">The **Get-AzApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="1265c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1265c-107">EXAMPLES</span></span>

### <span data-ttu-id="1265c-108">Przykład 1. Uzyskiwanie stanu ostatniej synchronizacji</span><span class="sxs-lookup"><span data-stu-id="1265c-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="1265c-109">To polecenie otrzymuje stan ostatniej synchronizacji między bazą danych konfiguracji a repozytorium Git.</span><span class="sxs-lookup"><span data-stu-id="1265c-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="1265c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1265c-110">PARAMETERS</span></span>

### <span data-ttu-id="1265c-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="1265c-111">-Context</span></span>
<span data-ttu-id="1265c-112">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="1265c-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1265c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1265c-113">-DefaultProfile</span></span>
<span data-ttu-id="1265c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1265c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1265c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1265c-115">CommonParameters</span></span>
<span data-ttu-id="1265c-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1265c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1265c-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1265c-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1265c-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1265c-118">INPUTS</span></span>

### <span data-ttu-id="1265c-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1265c-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="1265c-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1265c-120">OUTPUTS</span></span>

### <span data-ttu-id="1265c-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span><span class="sxs-lookup"><span data-stu-id="1265c-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="1265c-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1265c-122">NOTES</span></span>

## <span data-ttu-id="1265c-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1265c-123">RELATED LINKS</span></span>
