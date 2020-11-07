---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/get-azcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
ms.openlocfilehash: f046b9a57f0827977927e31d5009c6276cd89279
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706107"
---
# <span data-ttu-id="356bc-101">Get-AzContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="356bc-101">Get-AzContainerInstanceLog</span></span>

## <span data-ttu-id="356bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="356bc-102">SYNOPSIS</span></span>
<span data-ttu-id="356bc-103">Pobierz dzienniki wystąpienia kontenera w grupie kontenerów.</span><span class="sxs-lookup"><span data-stu-id="356bc-103">Get the logs of a container instance in a container group.</span></span>

## <span data-ttu-id="356bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="356bc-104">SYNTAX</span></span>

### <span data-ttu-id="356bc-105">GetContainerInstanceLogByNamesParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="356bc-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="356bc-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="356bc-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="356bc-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="356bc-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="356bc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="356bc-108">DESCRIPTION</span></span>
<span data-ttu-id="356bc-109">Polecenie cmdlet **Get-AzContainerInstanceLog** pobiera dzienniki kontenera w grupie kontenerowej.</span><span class="sxs-lookup"><span data-stu-id="356bc-109">The **Get-AzContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="356bc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="356bc-110">EXAMPLES</span></span>

### <span data-ttu-id="356bc-111">Przykład 1. Pobieranie dziennika końcowego wystąpienia kontenera</span><span class="sxs-lookup"><span data-stu-id="356bc-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="356bc-112">Pobierz dziennik z `container1` grupy kontenerowej `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="356bc-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="356bc-113">Domyślnie zwróci do 4 MB zawartości dziennika.</span><span class="sxs-lookup"><span data-stu-id="356bc-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="356bc-114">Przykład 2: pobieranie dziennika końcowego wystąpienia kontenera o takiej samej nazwie jak grupa kontenerów</span><span class="sxs-lookup"><span data-stu-id="356bc-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="356bc-115">Pobierz dziennik z `mycontainer` grupy kontenerowej `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="356bc-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="356bc-116">Domyślnie zwróci do 4 MB zawartości dziennika.</span><span class="sxs-lookup"><span data-stu-id="356bc-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="356bc-117">Przykład 3: pobieranie linii ogon 2 dziennika wystąpienia kontenera</span><span class="sxs-lookup"><span data-stu-id="356bc-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="356bc-118">Pobierz wiersze tail 2 dziennika z `container1` grupy kontenerów `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="356bc-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="356bc-119">Przykład 4: pobieranie dziennika końcowego wystąpienia kontenera w potoku w grupie kontener</span><span class="sxs-lookup"><span data-stu-id="356bc-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="356bc-120">Pobieranie dziennika z `mycontainer` potoku w grupie kontener `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="356bc-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="356bc-121">Domyślnie zwróci do 4 MB zawartości dziennika.</span><span class="sxs-lookup"><span data-stu-id="356bc-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="356bc-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="356bc-122">PARAMETERS</span></span>

### <span data-ttu-id="356bc-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="356bc-123">-ContainerGroupName</span></span>
<span data-ttu-id="356bc-124">Nazwa grupy kontenerów.</span><span class="sxs-lookup"><span data-stu-id="356bc-124">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="356bc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="356bc-125">-DefaultProfile</span></span>
<span data-ttu-id="356bc-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="356bc-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="356bc-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="356bc-127">-InputContainerGroup</span></span>
<span data-ttu-id="356bc-128">Wejściowy obiekt grupy kontenerowej.</span><span class="sxs-lookup"><span data-stu-id="356bc-128">The input container group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: GetContainerInstanceLogByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="356bc-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="356bc-129">-Name</span></span>
<span data-ttu-id="356bc-130">Nazwa wystąpienia kontenera w grupie kontener.</span><span class="sxs-lookup"><span data-stu-id="356bc-130">The container instance name in the container group.</span></span>
<span data-ttu-id="356bc-131">Wartość domyślna: tak samo jak nazwa grupy kontenerów</span><span class="sxs-lookup"><span data-stu-id="356bc-131">Default: the same as the container group name</span></span>

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

### <span data-ttu-id="356bc-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="356bc-132">-ResourceGroupName</span></span>
<span data-ttu-id="356bc-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="356bc-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="356bc-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="356bc-134">-ResourceId</span></span>
<span data-ttu-id="356bc-135">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="356bc-135">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="356bc-136">-Koniec</span><span class="sxs-lookup"><span data-stu-id="356bc-136">-Tail</span></span>
<span data-ttu-id="356bc-137">Liczba wierszy, w których ma się odogon dziennika.</span><span class="sxs-lookup"><span data-stu-id="356bc-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="356bc-138">Jeśli nie określono, polecenie cmdlet zwróci do ponad 4 MB dziennika końcowego.</span><span class="sxs-lookup"><span data-stu-id="356bc-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="356bc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="356bc-139">CommonParameters</span></span>
<span data-ttu-id="356bc-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="356bc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="356bc-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="356bc-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="356bc-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="356bc-142">INPUTS</span></span>

### <span data-ttu-id="356bc-143">Microsoft. Azure. Commands. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="356bc-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="356bc-144">System. String</span><span class="sxs-lookup"><span data-stu-id="356bc-144">System.String</span></span>

## <span data-ttu-id="356bc-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="356bc-145">OUTPUTS</span></span>

### <span data-ttu-id="356bc-146">System. String</span><span class="sxs-lookup"><span data-stu-id="356bc-146">System.String</span></span>

## <span data-ttu-id="356bc-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="356bc-147">NOTES</span></span>

## <span data-ttu-id="356bc-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="356bc-148">RELATED LINKS</span></span>
