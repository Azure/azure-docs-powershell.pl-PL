---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
ms.openlocfilehash: 233c74e3939884cd4bd311ec463d81d7e7613f31
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322313"
---
# <span data-ttu-id="e60cc-101">Get-AzApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="e60cc-101">Get-AzApiManagementTenantSyncState</span></span>

## <span data-ttu-id="e60cc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e60cc-102">SYNOPSIS</span></span>
<span data-ttu-id="e60cc-103">Pobiera stan ostatniej synchronizacji bazy danych konfiguracji i repozytorium git.</span><span class="sxs-lookup"><span data-stu-id="e60cc-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="e60cc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e60cc-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantSyncState -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e60cc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e60cc-105">DESCRIPTION</span></span>
<span data-ttu-id="e60cc-106">Polecenie cmdlet **Get-AzApiManagementTenantSyncState** Pobiera stan ostatniej synchronizacji bazy danych konfiguracji i repozytorium git.</span><span class="sxs-lookup"><span data-stu-id="e60cc-106">The **Get-AzApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="e60cc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e60cc-107">EXAMPLES</span></span>

### <span data-ttu-id="e60cc-108">Przykład 1: uzyskiwanie stanu ostatniej synchronizacji</span><span class="sxs-lookup"><span data-stu-id="e60cc-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="e60cc-109">To polecenie uzyskuje stan ostatniej synchronizacji między bazą danych konfiguracji a repozytorium git.</span><span class="sxs-lookup"><span data-stu-id="e60cc-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="e60cc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e60cc-110">PARAMETERS</span></span>

### <span data-ttu-id="e60cc-111">-Context</span><span class="sxs-lookup"><span data-stu-id="e60cc-111">-Context</span></span>
<span data-ttu-id="e60cc-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="e60cc-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e60cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e60cc-113">-DefaultProfile</span></span>
<span data-ttu-id="e60cc-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e60cc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e60cc-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e60cc-115">CommonParameters</span></span>
<span data-ttu-id="e60cc-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e60cc-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e60cc-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e60cc-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e60cc-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e60cc-118">INPUTS</span></span>

### <span data-ttu-id="e60cc-119">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e60cc-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="e60cc-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e60cc-120">OUTPUTS</span></span>

### <span data-ttu-id="e60cc-121">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementTenantConfigurationSyncState</span><span class="sxs-lookup"><span data-stu-id="e60cc-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="e60cc-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e60cc-122">NOTES</span></span>

## <span data-ttu-id="e60cc-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e60cc-123">RELATED LINKS</span></span>
