---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-azcloudserviceremotedesktopextensionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRemoteDesktopExtensionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRemoteDesktopExtensionObject.md
ms.openlocfilehash: 022093b8fe1df28a151405a18009b40dd24b0c97
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199419"
---
# <span data-ttu-id="d911e-101">New-AzCloudServiceRemoteDesktopExtensionObject</span><span class="sxs-lookup"><span data-stu-id="d911e-101">New-AzCloudServiceRemoteDesktopExtensionObject</span></span>

## <span data-ttu-id="d911e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d911e-102">SYNOPSIS</span></span>
<span data-ttu-id="d911e-103">Tworzenie obiektu w pamięci dla rozszerzenia pulpitu zdalnego</span><span class="sxs-lookup"><span data-stu-id="d911e-103">Create a in-memory object for Remote Desktop Extension</span></span>

## <span data-ttu-id="d911e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d911e-104">SYNTAX</span></span>

```
New-AzCloudServiceRemoteDesktopExtensionObject [-Name] <String> [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-TypeHandlerVersion] <String>] [[-RolesAppliedTo] <String[]>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [<CommonParameters>]
```

## <span data-ttu-id="d911e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d911e-105">DESCRIPTION</span></span>
<span data-ttu-id="d911e-106">Tworzenie obiektu w pamięci dla rozszerzenia pulpitu zdalnego</span><span class="sxs-lookup"><span data-stu-id="d911e-106">Create a in-memory object for Remote Desktop Extension</span></span>

## <span data-ttu-id="d911e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d911e-107">EXAMPLES</span></span>

### <span data-ttu-id="d911e-108">Przykład 1. Tworzenie obiektu rozszerzenia pulpitu zdalnego</span><span class="sxs-lookup"><span data-stu-id="d911e-108">Example 1: Create remote desktop extension object</span></span>
```powershell
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $extension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'
```

<span data-ttu-id="d911e-109">To polecenie tworzy obiekt rozszerzenia pulpitu zdalnego, który jest używany do tworzenia lub aktualizowania usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="d911e-109">This command creates remote desktop extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="d911e-110">Aby uzyskać więcej szczegółowych informacji, zobacz New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="d911e-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="d911e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d911e-111">PARAMETERS</span></span>

### <span data-ttu-id="d911e-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d911e-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="d911e-113">Wersja pomocnicza automatycznego uaktualniania.</span><span class="sxs-lookup"><span data-stu-id="d911e-113">Auto upgrade minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d911e-114">- Credential</span><span class="sxs-lookup"><span data-stu-id="d911e-114">-Credential</span></span>
<span data-ttu-id="d911e-115">Poświadczenia rozszerzenia pulpitu zdalnego.</span><span class="sxs-lookup"><span data-stu-id="d911e-115">Credential for Remote Desktop Extension.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d911e-116">— wygasanie</span><span class="sxs-lookup"><span data-stu-id="d911e-116">-Expiration</span></span>
<span data-ttu-id="d911e-117">Wygasanie rozszerzenia pulpitu zdalnego.</span><span class="sxs-lookup"><span data-stu-id="d911e-117">Expiration for Remote Desktop Extension.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d911e-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d911e-118">-Name</span></span>
<span data-ttu-id="d911e-119">Nazwa rozszerzenia pulpitu zdalnego.</span><span class="sxs-lookup"><span data-stu-id="d911e-119">Name of Remote Desktop Extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d911e-120">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="d911e-120">-RolesAppliedTo</span></span>
<span data-ttu-id="d911e-121">Role, do których zastosowano role.</span><span class="sxs-lookup"><span data-stu-id="d911e-121">Roles applied to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d911e-122">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d911e-122">-TypeHandlerVersion</span></span>
<span data-ttu-id="d911e-123">Wersja rozszerzenia pulpitu zdalnego.</span><span class="sxs-lookup"><span data-stu-id="d911e-123">Remote Desktop Extension version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d911e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d911e-124">CommonParameters</span></span>
<span data-ttu-id="d911e-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d911e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d911e-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d911e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d911e-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d911e-127">INPUTS</span></span>

## <span data-ttu-id="d911e-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d911e-128">OUTPUTS</span></span>

### <span data-ttu-id="d911e-129">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="d911e-129">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="d911e-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d911e-130">NOTES</span></span>

<span data-ttu-id="d911e-131">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d911e-131">ALIASES</span></span>

## <span data-ttu-id="d911e-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d911e-132">RELATED LINKS</span></span>

