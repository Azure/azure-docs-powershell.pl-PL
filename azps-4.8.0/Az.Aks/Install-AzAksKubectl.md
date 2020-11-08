---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/install-azakskubectl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
ms.openlocfilehash: 746efc579e1977e54a1898bbe183d951c3d9c21f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219663"
---
# <span data-ttu-id="6ca2c-101">Install-AzAksKubectl</span><span class="sxs-lookup"><span data-stu-id="6ca2c-101">Install-AzAksKubectl</span></span>

## <span data-ttu-id="6ca2c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ca2c-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca2c-103">Pobierz i zainstaluj kubectl, Kubernetes narzędzie wiersza polecenia.</span><span class="sxs-lookup"><span data-stu-id="6ca2c-103">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="6ca2c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ca2c-104">SYNTAX</span></span>

```
Install-AzAksKubectl [-Destination <String>] [-Version <String>] [-DownloadFromMirror] [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ca2c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6ca2c-105">DESCRIPTION</span></span>
<span data-ttu-id="6ca2c-106">Pobierz i zainstaluj kubectl, Kubernetes narzędzie wiersza polecenia.</span><span class="sxs-lookup"><span data-stu-id="6ca2c-106">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="6ca2c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ca2c-107">EXAMPLES</span></span>

### <span data-ttu-id="6ca2c-108">Pobieranie i Instalowanie najnowszej wersji programu kubectl</span><span class="sxs-lookup"><span data-stu-id="6ca2c-108">Download and install latest version of kubectl</span></span>
```powershell
PS C:\> Install-AzAksKubectl -Version latest
```

## <span data-ttu-id="6ca2c-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ca2c-109">PARAMETERS</span></span>

### <span data-ttu-id="6ca2c-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ca2c-110">-AsJob</span></span>
<span data-ttu-id="6ca2c-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6ca2c-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ca2c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca2c-112">-DefaultProfile</span></span>
<span data-ttu-id="6ca2c-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ca2c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ca2c-114">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="6ca2c-114">-Destination</span></span>
<span data-ttu-id="6ca2c-115">Ścieżka do instalacji kubectl.</span><span class="sxs-lookup"><span data-stu-id="6ca2c-115">Path at which to install kubectl.</span></span>
<span data-ttu-id="6ca2c-116">Domyślnie można instalować w usłudze ~/.Azure-kubectl/</span><span class="sxs-lookup"><span data-stu-id="6ca2c-116">Default to install into ~/.azure-kubectl/</span></span>

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

### <span data-ttu-id="6ca2c-117">-DownloadFromMirror</span><span class="sxs-lookup"><span data-stu-id="6ca2c-117">-DownloadFromMirror</span></span>
<span data-ttu-id="6ca2c-118">Pobierz ze strony lustrzanej: https://mirror.azure.cn/kubernetes/kubectl/</span><span class="sxs-lookup"><span data-stu-id="6ca2c-118">Download from mirror site : https://mirror.azure.cn/kubernetes/kubectl/</span></span>

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

### <span data-ttu-id="6ca2c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6ca2c-119">-Force</span></span>
<span data-ttu-id="6ca2c-120">Zastąp istniejące kubectl bez monitu</span><span class="sxs-lookup"><span data-stu-id="6ca2c-120">Overwrite existing kubectl without prompt</span></span>

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

### <span data-ttu-id="6ca2c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ca2c-121">-PassThru</span></span>
<span data-ttu-id="6ca2c-122">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6ca2c-122">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="6ca2c-123">-Version</span><span class="sxs-lookup"><span data-stu-id="6ca2c-123">-Version</span></span>
<span data-ttu-id="6ca2c-124">Wersja programu kubectl do zainstalowania, na przykład "v 1.17.2".</span><span class="sxs-lookup"><span data-stu-id="6ca2c-124">Version of kubectl to install, e.g. 'v1.17.2'.</span></span>
<span data-ttu-id="6ca2c-125">Wartość domyślna: Najpóźniejsza</span><span class="sxs-lookup"><span data-stu-id="6ca2c-125">Default value: Latest</span></span>

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

### <span data-ttu-id="6ca2c-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ca2c-126">-Confirm</span></span>
<span data-ttu-id="6ca2c-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ca2c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ca2c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ca2c-128">-WhatIf</span></span>
<span data-ttu-id="6ca2c-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ca2c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ca2c-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6ca2c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ca2c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca2c-131">CommonParameters</span></span>
<span data-ttu-id="6ca2c-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ca2c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca2c-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ca2c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca2c-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ca2c-134">INPUTS</span></span>

### <span data-ttu-id="6ca2c-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6ca2c-135">None</span></span>

## <span data-ttu-id="6ca2c-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ca2c-136">OUTPUTS</span></span>

### <span data-ttu-id="6ca2c-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6ca2c-137">System.Boolean</span></span>

## <span data-ttu-id="6ca2c-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ca2c-138">NOTES</span></span>

## <span data-ttu-id="6ca2c-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ca2c-139">RELATED LINKS</span></span>
