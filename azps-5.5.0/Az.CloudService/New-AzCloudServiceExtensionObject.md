---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceExtensionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceExtensionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceExtensionObject.md
ms.openlocfilehash: 761d34b4ed2d061b773c136a7d4e2db9f05a9103
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195138"
---
# <span data-ttu-id="e2f88-101">New-AzCloudServiceExtensionObject</span><span class="sxs-lookup"><span data-stu-id="e2f88-101">New-AzCloudServiceExtensionObject</span></span>

## <span data-ttu-id="e2f88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2f88-102">SYNOPSIS</span></span>
<span data-ttu-id="e2f88-103">Tworzenie obiektu w pamięci dla rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="e2f88-103">Create a in-memory object for Extension</span></span>

## <span data-ttu-id="e2f88-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e2f88-104">SYNTAX</span></span>

```
New-AzCloudServiceExtensionObject [-AutoUpgradeMinorVersion <Boolean>] [-Name <String>]
 [-ProtectedSetting <String>] [-Publisher <String>] [-RolesAppliedTo <String[]>] [-Setting <String>]
 [-Type <String>] [-TypeHandlerVersion <String>] [<CommonParameters>]
```

## <span data-ttu-id="e2f88-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e2f88-105">DESCRIPTION</span></span>
<span data-ttu-id="e2f88-106">Tworzenie obiektu w pamięci dla rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="e2f88-106">Create a in-memory object for Extension</span></span>

## <span data-ttu-id="e2f88-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e2f88-107">EXAMPLES</span></span>

### <span data-ttu-id="e2f88-108">Przykład 1. Tworzenie obiektu rozszerzenia Donicz</span><span class="sxs-lookup"><span data-stu-id="e2f88-108">Example 1: Create Geneva extension object</span></span>
```powershell
PS C:\> $extension = New-AzCloudServiceExtensionObject -Name "GenevaExtension" -Publisher "Microsoft.Azure.Geneva" -Type "GenevaMonitoringPaaS" -TypeHandlerVersion "2.14.0.2"
```

<span data-ttu-id="e2f88-109">To polecenie tworzy obiekt rozszerzenia Nasadka, który służy do tworzenia lub aktualizowania usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="e2f88-109">This command creates Geneva extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="e2f88-110">Aby uzyskać więcej szczegółowych informacji, zobacz New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="e2f88-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="e2f88-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2f88-111">PARAMETERS</span></span>

### <span data-ttu-id="e2f88-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="e2f88-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="e2f88-113">Jawnie określ, czy adres CRP może automatycznie uaktualniać typHandlerVersion do wyższych wersji pomocniczych, gdy staną się dostępne.</span><span class="sxs-lookup"><span data-stu-id="e2f88-113">Explicitly specify whether CRP can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f88-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e2f88-114">-Name</span></span>
<span data-ttu-id="e2f88-115">Nazwa.</span><span class="sxs-lookup"><span data-stu-id="e2f88-115">Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f88-116">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="e2f88-116">-ProtectedSetting</span></span>
<span data-ttu-id="e2f88-117">Ustawienia chronione rozszerzenia, które są szyfrowane przed ich wysłaniem do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e2f88-117">Protected settings for the extension which are encrypted before sent to the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f88-118">— Publisher</span><span class="sxs-lookup"><span data-stu-id="e2f88-118">-Publisher</span></span>
<span data-ttu-id="e2f88-119">Publisher.</span><span class="sxs-lookup"><span data-stu-id="e2f88-119">Publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f88-120">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="e2f88-120">-RolesAppliedTo</span></span>
<span data-ttu-id="e2f88-121">RolesAppliedTo.</span><span class="sxs-lookup"><span data-stu-id="e2f88-121">RolesAppliedTo.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f88-122">— Ustawienie</span><span class="sxs-lookup"><span data-stu-id="e2f88-122">-Setting</span></span>
<span data-ttu-id="e2f88-123">Ustawienia publiczne rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="e2f88-123">Public settings for the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f88-124">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="e2f88-124">-Type</span></span>
<span data-ttu-id="e2f88-125">Wpisz.</span><span class="sxs-lookup"><span data-stu-id="e2f88-125">Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f88-126">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="e2f88-126">-TypeHandlerVersion</span></span>
<span data-ttu-id="e2f88-127">TypeHandlerVersion.</span><span class="sxs-lookup"><span data-stu-id="e2f88-127">TypeHandlerVersion.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f88-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2f88-128">CommonParameters</span></span>
<span data-ttu-id="e2f88-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2f88-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2f88-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2f88-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2f88-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2f88-131">INPUTS</span></span>

## <span data-ttu-id="e2f88-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2f88-132">OUTPUTS</span></span>

### <span data-ttu-id="e2f88-133">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="e2f88-133">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="e2f88-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e2f88-134">NOTES</span></span>

<span data-ttu-id="e2f88-135">ALIASY</span><span class="sxs-lookup"><span data-stu-id="e2f88-135">ALIASES</span></span>

## <span data-ttu-id="e2f88-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2f88-136">RELATED LINKS</span></span>

