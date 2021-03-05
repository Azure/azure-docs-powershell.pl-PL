---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/get-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
ms.openlocfilehash: 82e5f6ced22b17c8966afbd5bc57324ab2069d1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991649"
---
# <span data-ttu-id="4e3ff-101">Get-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="4e3ff-101">Get-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="4e3ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e3ff-102">SYNOPSIS</span></span>
<span data-ttu-id="4e3ff-103">Uzyskiwanie kluczy dostępu zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="4e3ff-103">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="4e3ff-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4e3ff-104">SYNTAX</span></span>

```
Get-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4e3ff-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4e3ff-105">DESCRIPTION</span></span>
<span data-ttu-id="4e3ff-106">Uzyskiwanie kluczy dostępu zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="4e3ff-106">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="4e3ff-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4e3ff-107">EXAMPLES</span></span>

### <span data-ttu-id="4e3ff-108">Przykład 1. Pobieranie klucza dla określonej usługi communcation</span><span class="sxs-lookup"><span data-stu-id="4e3ff-108">Example 1: Fetch the Key for the specified Communcation service</span></span>
```powershell
PS C:\> Get-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

PrimaryConnectionString              PrimaryKey            SecondaryConnectionString               SecondaryKey
-----------------------              ----------            -----------------------                 ----------
endpoint=<example-primary-endpoint>  <example-primarykey>  endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="4e3ff-109">Wyświetla wartości ConnectionString i Key dla określonej usługi communcation.</span><span class="sxs-lookup"><span data-stu-id="4e3ff-109">Displays the ConnectionString and Key for the specified Communcation service.</span></span>

## <span data-ttu-id="4e3ff-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e3ff-110">PARAMETERS</span></span>

### <span data-ttu-id="4e3ff-111">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="4e3ff-111">-CommunicationServiceName</span></span>
<span data-ttu-id="4e3ff-112">Nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="4e3ff-112">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="4e3ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e3ff-113">-DefaultProfile</span></span>
<span data-ttu-id="4e3ff-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4e3ff-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e3ff-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e3ff-115">-ResourceGroupName</span></span>
<span data-ttu-id="4e3ff-116">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="4e3ff-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4e3ff-117">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="4e3ff-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="4e3ff-118">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e3ff-118">-SubscriptionId</span></span>
<span data-ttu-id="4e3ff-119">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4e3ff-119">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="4e3ff-120">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="4e3ff-120">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4e3ff-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4e3ff-121">-Confirm</span></span>
<span data-ttu-id="4e3ff-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4e3ff-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e3ff-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e3ff-123">-WhatIf</span></span>
<span data-ttu-id="4e3ff-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e3ff-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e3ff-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4e3ff-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e3ff-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e3ff-126">CommonParameters</span></span>
<span data-ttu-id="4e3ff-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e3ff-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e3ff-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e3ff-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e3ff-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e3ff-129">INPUTS</span></span>

## <span data-ttu-id="4e3ff-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e3ff-130">OUTPUTS</span></span>

### <span data-ttu-id="4e3ff-131">Microsoft.Azure.PowerShell.cmdlet.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="4e3ff-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="4e3ff-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4e3ff-132">NOTES</span></span>

<span data-ttu-id="4e3ff-133">ALIASY</span><span class="sxs-lookup"><span data-stu-id="4e3ff-133">ALIASES</span></span>

## <span data-ttu-id="4e3ff-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e3ff-134">RELATED LINKS</span></span>

