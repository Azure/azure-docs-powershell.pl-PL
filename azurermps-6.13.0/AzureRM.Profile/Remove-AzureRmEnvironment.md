---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
ms.openlocfilehash: 05a4b2a475b2bd58de706ba038f2760d133b7dbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547356"
---
# <span data-ttu-id="c8e10-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="c8e10-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="c8e10-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c8e10-102">SYNOPSIS</span></span>
<span data-ttu-id="c8e10-103">Umożliwia usunięcie punktów końcowych i metadanych w celu nawiązania połączenia z danym wystąpieniem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c8e10-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8e10-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c8e10-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8e10-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c8e10-105">DESCRIPTION</span></span>
<span data-ttu-id="c8e10-106">Polecenie cmdlet Remove-AzureRmEnvironment powoduje usunięcie punktów końcowych i informacji o metadanych w celu nawiązania połączenia z danym wystąpieniem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c8e10-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="c8e10-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c8e10-107">EXAMPLES</span></span>

### <span data-ttu-id="c8e10-108">Przykład 1: Tworzenie i usuwanie środowiska testowego</span><span class="sxs-lookup"><span data-stu-id="c8e10-108">Example 1: Creating and removing a test environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Remove-AzureRmEnvironment -Name TestEnvironment

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="c8e10-109">W tym przykładzie pokazano, jak utworzyć środowisko przy użyciu dodatku Add-AzureRmEnvironment, a następnie jak usunąć środowisko przy użyciu polecenia Remove-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="c8e10-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="c8e10-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8e10-110">PARAMETERS</span></span>

### <span data-ttu-id="c8e10-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8e10-111">-DefaultProfile</span></span>
<span data-ttu-id="c8e10-112">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c8e10-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8e10-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c8e10-113">-Name</span></span>
<span data-ttu-id="c8e10-114">Określa nazwę środowiska, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="c8e10-114">Specifies the name of the environment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8e10-115">-Zakres</span><span class="sxs-lookup"><span data-stu-id="c8e10-115">-Scope</span></span>
<span data-ttu-id="c8e10-116">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c8e10-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8e10-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c8e10-117">-Confirm</span></span>
<span data-ttu-id="c8e10-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8e10-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8e10-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8e10-119">-WhatIf</span></span>
<span data-ttu-id="c8e10-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8e10-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8e10-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c8e10-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8e10-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8e10-122">CommonParameters</span></span>
<span data-ttu-id="c8e10-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8e10-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8e10-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8e10-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8e10-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8e10-125">INPUTS</span></span>

### <span data-ttu-id="c8e10-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c8e10-126">System.String</span></span>

## <span data-ttu-id="c8e10-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c8e10-127">OUTPUTS</span></span>

### <span data-ttu-id="c8e10-128">Microsoft. Azure. Commands. profile. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="c8e10-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="c8e10-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c8e10-129">NOTES</span></span>

## <span data-ttu-id="c8e10-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8e10-130">RELATED LINKS</span></span>

[<span data-ttu-id="c8e10-131">Dodaj-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="c8e10-131">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="c8e10-132">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="c8e10-132">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="c8e10-133">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="c8e10-133">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

