---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/get-azurermcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
ms.openlocfilehash: 08a4ab0f0d937f06ee0ac958aa57a2f0eed5e4a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716448"
---
# <span data-ttu-id="3888e-101">Get-AzureRmContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="3888e-101">Get-AzureRmContainerInstanceLog</span></span>

## <span data-ttu-id="3888e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3888e-102">SYNOPSIS</span></span>
<span data-ttu-id="3888e-103">Pobierz dzienniki wystąpienia kontenera w grupie kontenerów.</span><span class="sxs-lookup"><span data-stu-id="3888e-103">Get the logs of a container instance in a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3888e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3888e-104">SYNTAX</span></span>

### <span data-ttu-id="3888e-105">GetContainerInstanceLogByNamesParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3888e-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzureRmContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3888e-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="3888e-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzureRmContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3888e-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="3888e-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzureRmContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3888e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3888e-108">DESCRIPTION</span></span>
<span data-ttu-id="3888e-109">Polecenie cmdlet **Get-AzureRmContainerInstanceLog** pobiera dzienniki kontenera w grupie kontenerowej.</span><span class="sxs-lookup"><span data-stu-id="3888e-109">The **Get-AzureRmContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="3888e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3888e-110">EXAMPLES</span></span>

### <span data-ttu-id="3888e-111">Przykład 1. Pobieranie dziennika końcowego wystąpienia kontenera</span><span class="sxs-lookup"><span data-stu-id="3888e-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="3888e-112">Pobierz dziennik z `container1` grupy kontenerowej `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="3888e-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="3888e-113">Domyślnie zwróci do 4 MB zawartości dziennika.</span><span class="sxs-lookup"><span data-stu-id="3888e-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="3888e-114">Przykład 2: pobieranie dziennika końcowego wystąpienia kontenera o takiej samej nazwie jak grupa kontenerów</span><span class="sxs-lookup"><span data-stu-id="3888e-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="3888e-115">Pobierz dziennik z `mycontainer` grupy kontenerowej `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="3888e-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="3888e-116">Domyślnie zwróci do 4 MB zawartości dziennika.</span><span class="sxs-lookup"><span data-stu-id="3888e-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="3888e-117">Przykład 3: pobieranie linii ogon 2 dziennika wystąpienia kontenera</span><span class="sxs-lookup"><span data-stu-id="3888e-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="3888e-118">Pobierz wiersze tail 2 dziennika z `container1` grupy kontenerów `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="3888e-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="3888e-119">Przykład 4: pobieranie dziennika końcowego wystąpienia kontenera w potoku w grupie kontener</span><span class="sxs-lookup"><span data-stu-id="3888e-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzureRmContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="3888e-120">Pobieranie dziennika z `mycontainer` potoku w grupie kontener `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="3888e-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="3888e-121">Domyślnie zwróci do 4 MB zawartości dziennika.</span><span class="sxs-lookup"><span data-stu-id="3888e-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="3888e-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3888e-122">PARAMETERS</span></span>

### <span data-ttu-id="3888e-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="3888e-123">-ContainerGroupName</span></span>
<span data-ttu-id="3888e-124">Nazwa grupy kontenerów.</span><span class="sxs-lookup"><span data-stu-id="3888e-124">The container group name.</span></span>

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

### <span data-ttu-id="3888e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3888e-125">-DefaultProfile</span></span>
<span data-ttu-id="3888e-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3888e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3888e-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="3888e-127">-InputContainerGroup</span></span>
<span data-ttu-id="3888e-128">Wejściowy obiekt grupy kontenerowej.</span><span class="sxs-lookup"><span data-stu-id="3888e-128">The input container group object.</span></span>

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

### <span data-ttu-id="3888e-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3888e-129">-Name</span></span>
<span data-ttu-id="3888e-130">Nazwa wystąpienia kontenera w grupie kontener.</span><span class="sxs-lookup"><span data-stu-id="3888e-130">The container instance name in the container group.</span></span>
<span data-ttu-id="3888e-131">Wartość domyślna: tak samo jak nazwa grupy kontenerów</span><span class="sxs-lookup"><span data-stu-id="3888e-131">Default: the same as the container group name</span></span>

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

### <span data-ttu-id="3888e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3888e-132">-ResourceGroupName</span></span>
<span data-ttu-id="3888e-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3888e-133">The resource group name.</span></span>

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

### <span data-ttu-id="3888e-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3888e-134">-ResourceId</span></span>
<span data-ttu-id="3888e-135">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="3888e-135">The resource id.</span></span>

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

### <span data-ttu-id="3888e-136">-Koniec</span><span class="sxs-lookup"><span data-stu-id="3888e-136">-Tail</span></span>
<span data-ttu-id="3888e-137">Liczba wierszy, w których ma się odogon dziennika.</span><span class="sxs-lookup"><span data-stu-id="3888e-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="3888e-138">Jeśli nie określono, polecenie cmdlet zwróci do ponad 4 MB dziennika końcowego.</span><span class="sxs-lookup"><span data-stu-id="3888e-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

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

### <span data-ttu-id="3888e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3888e-139">CommonParameters</span></span>
<span data-ttu-id="3888e-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3888e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3888e-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3888e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3888e-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3888e-142">INPUTS</span></span>

### <span data-ttu-id="3888e-143">Microsoft. Azure. Commands. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="3888e-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>
<span data-ttu-id="3888e-144">Parametry: InputContainerGroup (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3888e-144">Parameters: InputContainerGroup (ByValue)</span></span>

### <span data-ttu-id="3888e-145">System. String</span><span class="sxs-lookup"><span data-stu-id="3888e-145">System.String</span></span>

## <span data-ttu-id="3888e-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3888e-146">OUTPUTS</span></span>

### <span data-ttu-id="3888e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="3888e-147">System.String</span></span>

## <span data-ttu-id="3888e-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3888e-148">NOTES</span></span>

## <span data-ttu-id="3888e-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3888e-149">RELATED LINKS</span></span>
