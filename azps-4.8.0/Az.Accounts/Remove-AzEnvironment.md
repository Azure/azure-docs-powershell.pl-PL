---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
ms.openlocfilehash: 2c7ba44358db4e6a578f9876e26a099b2242badc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94224080"
---
# <span data-ttu-id="92a6c-101">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="92a6c-101">Remove-AzEnvironment</span></span>

## <span data-ttu-id="92a6c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92a6c-102">SYNOPSIS</span></span>
<span data-ttu-id="92a6c-103">Umożliwia usunięcie punktów końcowych i metadanych w celu nawiązania połączenia z danym wystąpieniem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="92a6c-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="92a6c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92a6c-104">SYNTAX</span></span>

```
Remove-AzEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92a6c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="92a6c-105">DESCRIPTION</span></span>
<span data-ttu-id="92a6c-106">Polecenie cmdlet Remove-AzEnvironment powoduje usunięcie punktów końcowych i informacji o metadanych w celu nawiązania połączenia z danym wystąpieniem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="92a6c-106">The Remove-AzEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="92a6c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92a6c-107">EXAMPLES</span></span>

### <span data-ttu-id="92a6c-108">Przykład 1: Tworzenie i usuwanie środowiska testowego</span><span class="sxs-lookup"><span data-stu-id="92a6c-108">Example 1: Creating and removing a test environment</span></span>
```
PS C:\> Add-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Remove-AzEnvironment -Name TestEnvironment

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="92a6c-109">W tym przykładzie pokazano, jak utworzyć środowisko przy użyciu dodatku Add-AzEnvironment, a następnie jak usunąć środowisko przy użyciu polecenia Remove-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="92a6c-109">This example shows how to create an environment using Add-AzEnvironment, and then how to delete the environment using Remove-AzEnvironment.</span></span>

## <span data-ttu-id="92a6c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92a6c-110">PARAMETERS</span></span>

### <span data-ttu-id="92a6c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92a6c-111">-DefaultProfile</span></span>
<span data-ttu-id="92a6c-112">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="92a6c-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92a6c-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="92a6c-113">-Name</span></span>
<span data-ttu-id="92a6c-114">Określa nazwę środowiska, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="92a6c-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="92a6c-115">-Zakres</span><span class="sxs-lookup"><span data-stu-id="92a6c-115">-Scope</span></span>
<span data-ttu-id="92a6c-116">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="92a6c-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="92a6c-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="92a6c-117">-Confirm</span></span>
<span data-ttu-id="92a6c-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92a6c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92a6c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92a6c-119">-WhatIf</span></span>
<span data-ttu-id="92a6c-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92a6c-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92a6c-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="92a6c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92a6c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92a6c-122">CommonParameters</span></span>
<span data-ttu-id="92a6c-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92a6c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92a6c-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92a6c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92a6c-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92a6c-125">INPUTS</span></span>

### <span data-ttu-id="92a6c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="92a6c-126">System.String</span></span>

## <span data-ttu-id="92a6c-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92a6c-127">OUTPUTS</span></span>

### <span data-ttu-id="92a6c-128">Microsoft. Azure. Commands. profile. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="92a6c-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="92a6c-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92a6c-129">NOTES</span></span>

## <span data-ttu-id="92a6c-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92a6c-130">RELATED LINKS</span></span>

[<span data-ttu-id="92a6c-131">Dodaj-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="92a6c-131">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="92a6c-132">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="92a6c-132">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="92a6c-133">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="92a6c-133">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

