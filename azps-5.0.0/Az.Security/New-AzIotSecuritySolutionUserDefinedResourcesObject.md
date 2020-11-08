---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionUserDefinedResourcesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
ms.openlocfilehash: e824c32ae2ae4f28972cdac9446eeeae6e410c75
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234275"
---
# <span data-ttu-id="34b0c-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span><span class="sxs-lookup"><span data-stu-id="34b0c-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span></span>

## <span data-ttu-id="34b0c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="34b0c-103">Tworzenie nowych zasobów zdefiniowanych przez użytkownika na potrzeby rozwiązania zabezpieczającego IoT</span><span class="sxs-lookup"><span data-stu-id="34b0c-103">Create new user defined resources for iot security solution</span></span>

## <span data-ttu-id="34b0c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34b0c-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionUserDefinedResourcesObject -Query <String> -QuerySubscriptionList <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34b0c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="34b0c-105">DESCRIPTION</span></span>
<span data-ttu-id="34b0c-106">Polecenie cmdlet AzIotSecuritySolutionUserDefinedResourcesObject tworzy nowy obiekt zasobów zdefiniowany przez użytkownika dla rozwiązania zabezpieczeń IoT.</span><span class="sxs-lookup"><span data-stu-id="34b0c-106">The AzIotSecuritySolutionUserDefinedResourcesObject cmdlet creates a new user defined resources object for the iot security solution.</span></span>

## <span data-ttu-id="34b0c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34b0c-107">EXAMPLES</span></span>

### <span data-ttu-id="34b0c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="34b0c-108">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")

Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
QuerySubscriptions: ["XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX"]
```

<span data-ttu-id="34b0c-109">Tworzenie nowych zasobów zdefiniowanych przez użytkownika</span><span class="sxs-lookup"><span data-stu-id="34b0c-109">Create new user defined resources</span></span>

## <span data-ttu-id="34b0c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34b0c-110">PARAMETERS</span></span>

### <span data-ttu-id="34b0c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34b0c-111">-DefaultProfile</span></span>
<span data-ttu-id="34b0c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="34b0c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34b0c-113">-Query</span><span class="sxs-lookup"><span data-stu-id="34b0c-113">-Query</span></span>
<span data-ttu-id="34b0c-114">Microsoft.</span><span class="sxs-lookup"><span data-stu-id="34b0c-114">Query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34b0c-115">-QuerySubscriptionList</span><span class="sxs-lookup"><span data-stu-id="34b0c-115">-QuerySubscriptionList</span></span>
<span data-ttu-id="34b0c-116">Subskrypcje kwerend.</span><span class="sxs-lookup"><span data-stu-id="34b0c-116">Query subscriptions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34b0c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34b0c-117">CommonParameters</span></span>
<span data-ttu-id="34b0c-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34b0c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34b0c-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34b0c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34b0c-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34b0c-120">INPUTS</span></span>

### <span data-ttu-id="34b0c-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="34b0c-121">None</span></span>

## <span data-ttu-id="34b0c-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34b0c-122">OUTPUTS</span></span>

### <span data-ttu-id="34b0c-123">Microsoft. Azure. Commands. Security. models. IotSecuritySolutions. PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="34b0c-123">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

## <span data-ttu-id="34b0c-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34b0c-124">NOTES</span></span>

## <span data-ttu-id="34b0c-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34b0c-125">RELATED LINKS</span></span>
