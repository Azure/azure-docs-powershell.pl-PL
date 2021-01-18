---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/get-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
ms.openlocfilehash: e4a16b69e5919684b40d5b9f7fd4e97465d3565e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501967"
---
# <span data-ttu-id="9e5f3-101">Get-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="9e5f3-101">Get-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="9e5f3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e5f3-102">SYNOPSIS</span></span>
<span data-ttu-id="9e5f3-103">Uzyskiwanie klawiszy dostępu do zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-103">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="9e5f3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e5f3-104">SYNTAX</span></span>

```
Get-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9e5f3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9e5f3-105">DESCRIPTION</span></span>
<span data-ttu-id="9e5f3-106">Uzyskiwanie klawiszy dostępu do zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-106">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="9e5f3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e5f3-107">EXAMPLES</span></span>

### <span data-ttu-id="9e5f3-108">Przykład 1: Pobieranie klucza dla określonej usługi komunikacji</span><span class="sxs-lookup"><span data-stu-id="9e5f3-108">Example 1: Fetch the Key for the specified Communcation service</span></span>
```powershell
PS C:\> Get-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

PrimaryConnectionString              PrimaryKey            SecondaryConnectionString               SecondaryKey
-----------------------              ----------            -----------------------                 ----------
endpoint=<example-primary-endpoint>  <example-primarykey>  endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="9e5f3-109">Wyświetla parametry ConnectionString i Key określonej usługi komunikacji.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-109">Displays the ConnectionString and Key for the specified Communcation service.</span></span>

## <span data-ttu-id="9e5f3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e5f3-110">PARAMETERS</span></span>

### <span data-ttu-id="9e5f3-111">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="9e5f3-111">-CommunicationServiceName</span></span>
<span data-ttu-id="9e5f3-112">Nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-112">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="9e5f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e5f3-113">-DefaultProfile</span></span>
<span data-ttu-id="9e5f3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e5f3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e5f3-115">-ResourceGroupName</span></span>
<span data-ttu-id="9e5f3-116">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="9e5f3-117">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="9e5f3-118">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9e5f3-118">-SubscriptionId</span></span>
<span data-ttu-id="9e5f3-119">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-119">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="9e5f3-120">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-120">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9e5f3-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9e5f3-121">-Confirm</span></span>
<span data-ttu-id="9e5f3-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e5f3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e5f3-123">-WhatIf</span></span>
<span data-ttu-id="9e5f3-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e5f3-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e5f3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e5f3-126">CommonParameters</span></span>
<span data-ttu-id="9e5f3-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e5f3-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e5f3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e5f3-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e5f3-129">INPUTS</span></span>

## <span data-ttu-id="9e5f3-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e5f3-130">OUTPUTS</span></span>

### <span data-ttu-id="9e5f3-131">Microsoft. Azure. PowerShell. cmdlet. Communication. models. Api20200820Preview. ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="9e5f3-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="9e5f3-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e5f3-132">NOTES</span></span>

<span data-ttu-id="9e5f3-133">PISUJE</span><span class="sxs-lookup"><span data-stu-id="9e5f3-133">ALIASES</span></span>

## <span data-ttu-id="9e5f3-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e5f3-134">RELATED LINKS</span></span>

