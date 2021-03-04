---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/remove-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
ms.openlocfilehash: 5acba21e8daf1adaa83820d67c5955b27230c4ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954913"
---
# <span data-ttu-id="721d4-101">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="721d4-101">Remove-AzEnvironment</span></span>

## <span data-ttu-id="721d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="721d4-102">SYNOPSIS</span></span>
<span data-ttu-id="721d4-103">Usuwa punkty końcowe i metadane na celu połączenie się z danym wystąpieniem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="721d4-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="721d4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="721d4-104">SYNTAX</span></span>

```
Remove-AzEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="721d4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="721d4-105">DESCRIPTION</span></span>
<span data-ttu-id="721d4-106">To Remove-AzEnvironment cmdlet usuwa punkty końcowe i informacje metadanych na temat łączenia się z danym wystąpieniem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="721d4-106">The Remove-AzEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="721d4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="721d4-107">EXAMPLES</span></span>

### <span data-ttu-id="721d4-108">Przykład 1. Tworzenie i usuwanie środowiska testowego</span><span class="sxs-lookup"><span data-stu-id="721d4-108">Example 1: Creating and removing a test environment</span></span>
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

<span data-ttu-id="721d4-109">W tym przykładzie pokazano, jak utworzyć środowisko przy użyciu narzędzia Add-AzEnvironment, a następnie jak usunąć to środowisko za pomocą narzędzia Remove-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="721d4-109">This example shows how to create an environment using Add-AzEnvironment, and then how to delete the environment using Remove-AzEnvironment.</span></span>

## <span data-ttu-id="721d4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="721d4-110">PARAMETERS</span></span>

### <span data-ttu-id="721d4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="721d4-111">-DefaultProfile</span></span>
<span data-ttu-id="721d4-112">Poświadczenia, dzierżawy i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="721d4-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="721d4-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="721d4-113">-Name</span></span>
<span data-ttu-id="721d4-114">Określa nazwę środowiska do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="721d4-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="721d4-115">— Zakres</span><span class="sxs-lookup"><span data-stu-id="721d4-115">-Scope</span></span>
<span data-ttu-id="721d4-116">Określa zakres zmian kontekstu, na przykład tego, czy zmiany mają zastosowanie tylko do bieżącego procesu, czy do wszystkich sesji rozpoczętych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="721d4-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="721d4-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="721d4-117">-Confirm</span></span>
<span data-ttu-id="721d4-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="721d4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="721d4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="721d4-119">-WhatIf</span></span>
<span data-ttu-id="721d4-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="721d4-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="721d4-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="721d4-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="721d4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="721d4-122">CommonParameters</span></span>
<span data-ttu-id="721d4-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="721d4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="721d4-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="721d4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="721d4-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="721d4-125">INPUTS</span></span>

### <span data-ttu-id="721d4-126">System.String</span><span class="sxs-lookup"><span data-stu-id="721d4-126">System.String</span></span>

## <span data-ttu-id="721d4-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="721d4-127">OUTPUTS</span></span>

### <span data-ttu-id="721d4-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="721d4-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="721d4-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="721d4-129">NOTES</span></span>

## <span data-ttu-id="721d4-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="721d4-130">RELATED LINKS</span></span>

[<span data-ttu-id="721d4-131">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="721d4-131">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="721d4-132">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="721d4-132">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="721d4-133">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="721d4-133">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

