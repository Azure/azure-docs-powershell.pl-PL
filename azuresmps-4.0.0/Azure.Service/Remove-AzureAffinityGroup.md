---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 29602F63-A05B-45AF-8DD8-5EBBF4C33FCE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32af8d2e89c14b0d36265efc688a88858851bba5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055138"
---
# <span data-ttu-id="1e761-101">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="1e761-101">Remove-AzureAffinityGroup</span></span>

## <span data-ttu-id="1e761-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1e761-102">SYNOPSIS</span></span>
<span data-ttu-id="1e761-103">Usuwa grupę koligacji w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="1e761-103">Deletes an affinity group in a subscription.</span></span>

## <span data-ttu-id="1e761-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1e761-104">SYNTAX</span></span>

```
Remove-AzureAffinityGroup [-Name] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1e761-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1e761-105">DESCRIPTION</span></span>
<span data-ttu-id="1e761-106">Polecenie cmdlet **Remove-AzureAffinityGroup** usuwa grupę koligacji platformy Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1e761-106">The **Remove-AzureAffinityGroup** cmdlet deletes an Azure affinity group in the current subscription.</span></span>
<span data-ttu-id="1e761-107">Nie można usunąć grupy koligacji zawierającej żadnych członków.</span><span class="sxs-lookup"><span data-stu-id="1e761-107">You cannot delete an affinity group that has any members.</span></span>
<span data-ttu-id="1e761-108">Musisz najpierw usunąć wszystkich członków grupy koligacji.</span><span class="sxs-lookup"><span data-stu-id="1e761-108">You must first delete all the members of an affinity group.</span></span>

## <span data-ttu-id="1e761-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1e761-109">EXAMPLES</span></span>

### <span data-ttu-id="1e761-110">Przykład 1. Usuń grupę koligacji</span><span class="sxs-lookup"><span data-stu-id="1e761-110">Example 1: Remove an affinity group</span></span>
```
PS C:\> Remove-AzureAffinityGroup -Name "South01"
```

<span data-ttu-id="1e761-111">To polecenie usuwa grupę koligacji South01 w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1e761-111">This command deletes the South01 affinity group in the current subscription.</span></span>

## <span data-ttu-id="1e761-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1e761-112">PARAMETERS</span></span>

### <span data-ttu-id="1e761-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1e761-113">-InformationAction</span></span>
<span data-ttu-id="1e761-114">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="1e761-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1e761-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1e761-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1e761-116">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="1e761-116">Continue</span></span>
- <span data-ttu-id="1e761-117">Ignorować</span><span class="sxs-lookup"><span data-stu-id="1e761-117">Ignore</span></span>
- <span data-ttu-id="1e761-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="1e761-118">Inquire</span></span>
- <span data-ttu-id="1e761-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1e761-119">SilentlyContinue</span></span>
- <span data-ttu-id="1e761-120">Przestaw</span><span class="sxs-lookup"><span data-stu-id="1e761-120">Stop</span></span>
- <span data-ttu-id="1e761-121">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="1e761-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e761-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1e761-122">-InformationVariable</span></span>
<span data-ttu-id="1e761-123">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="1e761-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e761-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1e761-124">-Name</span></span>
<span data-ttu-id="1e761-125">Określa nazwę grupy koligacji, którą to polecenie cmdlet usuwa.</span><span class="sxs-lookup"><span data-stu-id="1e761-125">Specifies the name of the affinity group that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e761-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="1e761-126">-Profile</span></span>
<span data-ttu-id="1e761-127">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e761-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1e761-128">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="1e761-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e761-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e761-129">CommonParameters</span></span>
<span data-ttu-id="1e761-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e761-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e761-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e761-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e761-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e761-132">INPUTS</span></span>

## <span data-ttu-id="1e761-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1e761-133">OUTPUTS</span></span>

## <span data-ttu-id="1e761-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1e761-134">NOTES</span></span>

## <span data-ttu-id="1e761-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e761-135">RELATED LINKS</span></span>

[<span data-ttu-id="1e761-136">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="1e761-136">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="1e761-137">Nowe — AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="1e761-137">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="1e761-138">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="1e761-138">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


