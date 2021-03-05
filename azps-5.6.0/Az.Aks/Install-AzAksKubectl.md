---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/install-azakskubectl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
ms.openlocfilehash: 6a3dc975c34d4938235ce95743f73f833a948b49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966849"
---
# <span data-ttu-id="5689f-101">Install-AzAksKubectl</span><span class="sxs-lookup"><span data-stu-id="5689f-101">Install-AzAksKubectl</span></span>

## <span data-ttu-id="5689f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5689f-102">SYNOPSIS</span></span>
<span data-ttu-id="5689f-103">Pobierz i zainstaluj kubectl, narzędzie wiersza polecenia Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="5689f-103">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="5689f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5689f-104">SYNTAX</span></span>

```
Install-AzAksKubectl [-Destination <String>] [-Version <String>] [-DownloadFromMirror] [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5689f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5689f-105">DESCRIPTION</span></span>
<span data-ttu-id="5689f-106">Pobierz i zainstaluj kubectl, narzędzie wiersza polecenia Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="5689f-106">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="5689f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5689f-107">EXAMPLES</span></span>

### <span data-ttu-id="5689f-108">Pobieranie i instalowanie najnowszej wersji pliku kubectl</span><span class="sxs-lookup"><span data-stu-id="5689f-108">Download and install latest version of kubectl</span></span>
```powershell
PS C:\> Install-AzAksKubectl -Version latest
```

## <span data-ttu-id="5689f-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5689f-109">PARAMETERS</span></span>

### <span data-ttu-id="5689f-110">— AsJob</span><span class="sxs-lookup"><span data-stu-id="5689f-110">-AsJob</span></span>
<span data-ttu-id="5689f-111">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5689f-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5689f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5689f-112">-DefaultProfile</span></span>
<span data-ttu-id="5689f-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5689f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5689f-114">— miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="5689f-114">-Destination</span></span>
<span data-ttu-id="5689f-115">Ścieżka instalacji pliku kubectl.</span><span class="sxs-lookup"><span data-stu-id="5689f-115">Path at which to install kubectl.</span></span>
<span data-ttu-id="5689f-116">Domyślne instalowanie w ~/.azure-kubectl/</span><span class="sxs-lookup"><span data-stu-id="5689f-116">Default to install into ~/.azure-kubectl/</span></span>

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

### <span data-ttu-id="5689f-117">-DownloadFromMirror</span><span class="sxs-lookup"><span data-stu-id="5689f-117">-DownloadFromMirror</span></span>
<span data-ttu-id="5689f-118">Pobierz z witryny lustrzanej: https://mirror.azure.cn/kubernetes/kubectl/</span><span class="sxs-lookup"><span data-stu-id="5689f-118">Download from mirror site : https://mirror.azure.cn/kubernetes/kubectl/</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5689f-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="5689f-119">-Force</span></span>
<span data-ttu-id="5689f-120">Zastępowanie istniejącego kubectla bez monitu</span><span class="sxs-lookup"><span data-stu-id="5689f-120">Overwrite existing kubectl without prompt</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5689f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5689f-121">-PassThru</span></span>
<span data-ttu-id="5689f-122">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="5689f-122">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5689f-123">— Wersja</span><span class="sxs-lookup"><span data-stu-id="5689f-123">-Version</span></span>
<span data-ttu-id="5689f-124">Wersja kubectl do zainstalowania, np. '1.17.2'.</span><span class="sxs-lookup"><span data-stu-id="5689f-124">Version of kubectl to install, e.g. 'v1.17.2'.</span></span>
<span data-ttu-id="5689f-125">Wartość domyślna: najpóźniejsza</span><span class="sxs-lookup"><span data-stu-id="5689f-125">Default value: Latest</span></span>

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

### <span data-ttu-id="5689f-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5689f-126">-Confirm</span></span>
<span data-ttu-id="5689f-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5689f-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5689f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5689f-128">-WhatIf</span></span>
<span data-ttu-id="5689f-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5689f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5689f-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5689f-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5689f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5689f-131">CommonParameters</span></span>
<span data-ttu-id="5689f-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5689f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5689f-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5689f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5689f-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5689f-134">INPUTS</span></span>

### <span data-ttu-id="5689f-135">Brak</span><span class="sxs-lookup"><span data-stu-id="5689f-135">None</span></span>

## <span data-ttu-id="5689f-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5689f-136">OUTPUTS</span></span>

### <span data-ttu-id="5689f-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5689f-137">System.Boolean</span></span>

## <span data-ttu-id="5689f-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5689f-138">NOTES</span></span>

## <span data-ttu-id="5689f-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5689f-139">RELATED LINKS</span></span>
