---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
ms.openlocfilehash: 72273a95447f9ab0b10460952bc4b26312b9efdb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708063"
---
# <span data-ttu-id="4a6a8-101">Get-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="4a6a8-101">Get-AzSignalRKey</span></span>

## <span data-ttu-id="4a6a8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4a6a8-102">SYNOPSIS</span></span>
<span data-ttu-id="4a6a8-103">Uzyskaj klucze dostępu do usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="4a6a8-103">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="4a6a8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4a6a8-104">SYNTAX</span></span>

### <span data-ttu-id="4a6a8-105">ResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4a6a8-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a6a8-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a6a8-106">ResourceIdParameterSet</span></span>
```
Get-AzSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a6a8-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a6a8-107">InputObjectParameterSet</span></span>
```
Get-AzSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a6a8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4a6a8-108">DESCRIPTION</span></span>
<span data-ttu-id="4a6a8-109">Uzyskaj klucze dostępu do usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="4a6a8-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="4a6a8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4a6a8-110">EXAMPLES</span></span>

### <span data-ttu-id="4a6a8-111">Uzyskiwanie klawiszy dostępu dla konkretnej usługi sygnalizacji</span><span class="sxs-lookup"><span data-stu-id="4a6a8-111">Get access keys of a specific SignalR service</span></span>
```powershell
PS C:\> Get-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

### <span data-ttu-id="4a6a8-112">Uzyskiwanie kluczy dostępu z obiektu usługi sygnalizacji w potoku</span><span class="sxs-lookup"><span data-stu-id="4a6a8-112">Get access keys from a SignalR service object in pipe</span></span>

```powershell
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 | Get-AzSignalRKey

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

## <span data-ttu-id="4a6a8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a6a8-113">PARAMETERS</span></span>

### <span data-ttu-id="4a6a8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a6a8-114">-DefaultProfile</span></span>
<span data-ttu-id="4a6a8-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a6a8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a6a8-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4a6a8-116">-InputObject</span></span>
<span data-ttu-id="4a6a8-117">Obiekt zasobu sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="4a6a8-117">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a6a8-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4a6a8-118">-Name</span></span>
<span data-ttu-id="4a6a8-119">Nazwa usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="4a6a8-119">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6a8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a6a8-120">-ResourceGroupName</span></span>
<span data-ttu-id="4a6a8-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4a6a8-121">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6a8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a6a8-122">-ResourceId</span></span>
<span data-ttu-id="4a6a8-123">Identyfikator zasobu usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="4a6a8-123">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a6a8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a6a8-124">CommonParameters</span></span>
<span data-ttu-id="4a6a8-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a6a8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a6a8-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a6a8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a6a8-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a6a8-127">INPUTS</span></span>

### <span data-ttu-id="4a6a8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4a6a8-128">System.String</span></span>

### <span data-ttu-id="4a6a8-129">Microsoft. Azure. Commands. Signals. modele. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="4a6a8-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="4a6a8-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4a6a8-130">OUTPUTS</span></span>

### <span data-ttu-id="4a6a8-131">Microsoft. Azure. Commands. Signals. modele. PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="4a6a8-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>

## <span data-ttu-id="4a6a8-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4a6a8-132">NOTES</span></span>

## <span data-ttu-id="4a6a8-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a6a8-133">RELATED LINKS</span></span>
