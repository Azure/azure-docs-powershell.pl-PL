---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
ms.openlocfilehash: b9d7426bf275571d025ec0fef3f8bbec7c119c0b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552460"
---
# <span data-ttu-id="de782-101">Get-AzureRmApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="de782-101">Get-AzureRmApiManagementTenantSyncState</span></span>

## <span data-ttu-id="de782-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="de782-102">SYNOPSIS</span></span>
<span data-ttu-id="de782-103">Pobiera stan ostatniej synchronizacji bazy danych konfiguracji i repozytorium git.</span><span class="sxs-lookup"><span data-stu-id="de782-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de782-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="de782-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantSyncState -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de782-105">Opis</span><span class="sxs-lookup"><span data-stu-id="de782-105">DESCRIPTION</span></span>
<span data-ttu-id="de782-106">Polecenie cmdlet **Get-AzureRmApiManagementTenantSyncState** Pobiera stan ostatniej synchronizacji bazy danych konfiguracji i repozytorium git.</span><span class="sxs-lookup"><span data-stu-id="de782-106">The **Get-AzureRmApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="de782-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="de782-107">EXAMPLES</span></span>

### <span data-ttu-id="de782-108">Przykład 1: uzyskiwanie stanu ostatniej synchronizacji</span><span class="sxs-lookup"><span data-stu-id="de782-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>Get-AzureRmApiManagementTenantSyncState -Context $ApimContext
```

<span data-ttu-id="de782-109">To polecenie uzyskuje stan ostatniej synchronizacji między bazą danych konfiguracji a repozytorium git.</span><span class="sxs-lookup"><span data-stu-id="de782-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="de782-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="de782-110">PARAMETERS</span></span>

### <span data-ttu-id="de782-111">-Context</span><span class="sxs-lookup"><span data-stu-id="de782-111">-Context</span></span>
<span data-ttu-id="de782-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="de782-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="de782-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de782-113">-DefaultProfile</span></span>
<span data-ttu-id="de782-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="de782-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de782-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de782-115">CommonParameters</span></span>
<span data-ttu-id="de782-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de782-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de782-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de782-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de782-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de782-118">INPUTS</span></span>

## <span data-ttu-id="de782-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="de782-119">OUTPUTS</span></span>

### <span data-ttu-id="de782-120">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="de782-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="de782-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="de782-121">NOTES</span></span>

## <span data-ttu-id="de782-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de782-122">RELATED LINKS</span></span>

