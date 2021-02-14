---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceroleinstanceremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceRemoteDesktopFile.md
ms.openlocfilehash: 2b4133942a3aa7c4e9339579465942ade96c5709
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181795"
---
# <span data-ttu-id="d3eb4-101">Get-AzCloudServiceRoleInstanceRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="d3eb4-101">Get-AzCloudServiceRoleInstanceRemoteDesktopFile</span></span>

## <span data-ttu-id="d3eb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="d3eb4-103">Pobiera plik pulpitu zdalnego dla wystąpienia roli w usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="d3eb4-103">Gets a remote desktop file for a role instance in a cloud service.</span></span>

## <span data-ttu-id="d3eb4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d3eb4-104">SYNTAX</span></span>

```
Get-AzCloudServiceRoleInstanceRemoteDesktopFile -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> -OutFile <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

## <span data-ttu-id="d3eb4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d3eb4-105">DESCRIPTION</span></span>
<span data-ttu-id="d3eb4-106">Pobiera plik pulpitu zdalnego dla wystąpienia roli w usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="d3eb4-106">Gets a remote desktop file for a role instance in a cloud service.</span></span>

## <span data-ttu-id="d3eb4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d3eb4-107">EXAMPLES</span></span>

### <span data-ttu-id="d3eb4-108">Przykład 1. Uzyskiwanie pliku RDP</span><span class="sxs-lookup"><span data-stu-id="d3eb4-108">Example 1: Get an RDP file</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstanceRemoteDesktopFile -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0" -OutFile "C:\temp\ContosoFrontEnd_IN_0.rdp"
```

<span data-ttu-id="d3eb4-109">To polecenie pobiera plik RDP dla wystąpienia roli o nazwie ContosoFrontEnd IN 0 usługi w chmurze o nazwie ContosoCS, który należy do grupy zasobów \_ \_ o nazwie ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="d3eb4-109">This command gets an RDP file for the role instance named ContosoFrontEnd\_IN\_0 of cloud Service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="d3eb4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3eb4-110">PARAMETERS</span></span>

### <span data-ttu-id="d3eb4-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="d3eb4-111">-CloudServiceName</span></span>
<span data-ttu-id="d3eb4-112">.</span><span class="sxs-lookup"><span data-stu-id="d3eb4-112">.</span></span>

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

### <span data-ttu-id="d3eb4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3eb4-113">-DefaultProfile</span></span>
<span data-ttu-id="d3eb4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d3eb4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3eb4-115">-OutFile</span><span class="sxs-lookup"><span data-stu-id="d3eb4-115">-OutFile</span></span>
<span data-ttu-id="d3eb4-116">Ścieżka zapisu pliku wyjściowego w</span><span class="sxs-lookup"><span data-stu-id="d3eb4-116">Path to write output file to</span></span>

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

### <span data-ttu-id="d3eb4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3eb4-117">-PassThru</span></span>
<span data-ttu-id="d3eb4-118">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="d3eb4-118">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d3eb4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3eb4-119">-ResourceGroupName</span></span>
<span data-ttu-id="d3eb4-120">.</span><span class="sxs-lookup"><span data-stu-id="d3eb4-120">.</span></span>

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

### <span data-ttu-id="d3eb4-121">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="d3eb4-121">-RoleInstanceName</span></span>
<span data-ttu-id="d3eb4-122">Nazwa wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="d3eb4-122">Name of the role instance.</span></span>

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

### <span data-ttu-id="d3eb4-123">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d3eb4-123">-SubscriptionId</span></span>
<span data-ttu-id="d3eb4-124">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d3eb4-124">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d3eb4-125">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="d3eb4-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3eb4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3eb4-126">CommonParameters</span></span>
<span data-ttu-id="d3eb4-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3eb4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3eb4-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3eb4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3eb4-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3eb4-129">INPUTS</span></span>

## <span data-ttu-id="d3eb4-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d3eb4-130">OUTPUTS</span></span>

### <span data-ttu-id="d3eb4-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d3eb4-131">System.Boolean</span></span>

## <span data-ttu-id="d3eb4-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d3eb4-132">NOTES</span></span>

<span data-ttu-id="d3eb4-133">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d3eb4-133">ALIASES</span></span>

## <span data-ttu-id="d3eb4-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3eb4-134">RELATED LINKS</span></span>

