---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CE618AD2-7E28-4012-BF3C-B932B95FFDD5
online version: ''
schema: 2.0.0
ms.openlocfilehash: a07358c37bf30e8d5fc3040cdfd174b800df96e4
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061882"
---
# <span data-ttu-id="0dd1a-101">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="0dd1a-101">Remove-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="0dd1a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0dd1a-102">SYNOPSIS</span></span>
<span data-ttu-id="0dd1a-103">Usuwa obiekty statycznej puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="0dd1a-103">Removes static IP address pool objects.</span></span>

## <span data-ttu-id="0dd1a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0dd1a-104">SYNTAX</span></span>

```
Remove-WAPackStaticIPAddressPool -StaticIPAddressPool <StaticIPAddressPool> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0dd1a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0dd1a-105">DESCRIPTION</span></span>
<span data-ttu-id="0dd1a-106">Te tematy są przestarzałe i zostaną usunięte w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="0dd1a-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="0dd1a-107">W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0dd1a-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0dd1a-108">Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0dd1a-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0dd1a-109">Polecenie cmdlet **Remove-WAPackStaticIPAddressPool** usuwa obiekty statyczne puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="0dd1a-109">The **Remove-WAPackStaticIPAddressPool** cmdlet removes static IP address pool objects.</span></span>

## <span data-ttu-id="0dd1a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0dd1a-110">EXAMPLES</span></span>

### <span data-ttu-id="0dd1a-111">Przykład 1: Usuwanie puli statycznych adresów IP</span><span class="sxs-lookup"><span data-stu-id="0dd1a-111">Example 1: Remove a static IP address pool</span></span>
```
PS C:\> $StaticIPAddressPool = Get-WAPackStaticIPAddressPool -Name "ContosoStaticIPAddressPool01"
PS C:\> Remove-WAPackStaticIPAddressPool -StaticIPAddressPool $StaticIPAddressPool
```

<span data-ttu-id="0dd1a-112">Pierwsze polecenie pobiera statyczną pulę adresów IP o nazwie ContosoStaticIPAddressPool01 przy użyciu polecenia cmdlet **Get-WAPackStaticIPAddressPool** , a następnie zapisuje ten obiekt w zmiennej $StaticIPAddressPool.</span><span class="sxs-lookup"><span data-stu-id="0dd1a-112">The first command gets the static IP address pool named ContosoStaticIPAddressPool01 by using the **Get-WAPackStaticIPAddressPool** cmdlet, and then stores that object in the $StaticIPAddressPool variable.</span></span>

<span data-ttu-id="0dd1a-113">Drugie polecenie usuwa statyczną pulę adresów IP przechowywaną w $StaticIPAddressPool.</span><span class="sxs-lookup"><span data-stu-id="0dd1a-113">The second command removes the static IP address pool stored in $StaticIPAddressPool.</span></span>
<span data-ttu-id="0dd1a-114">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0dd1a-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="0dd1a-115">Przykład 2: usunięcie puli statycznych adresów IP bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="0dd1a-115">Example 2: Remove a static IP address pool without confirmation</span></span>
```
PS C:\> $StaticIPAddressPool = Get-WAPackStaticIPAddressPool -Name "ContosoStaticIPAddressPool02"
PS C:\> Remove-WAPackStaticIPAddressPool -StaticIPAddressPool $StaticIPAddressPool -Force
```

<span data-ttu-id="0dd1a-116">Pierwsze polecenie pobiera statyczną pulę adresów IP o nazwie ContosoStaticIPAddressPool02 przy użyciu polecenia cmdlet **Get-WAPackStaticIPAddressPool** , a następnie zapisuje ten obiekt w zmiennej $ StaticIPAddressPool.</span><span class="sxs-lookup"><span data-stu-id="0dd1a-116">The first command gets the static IP address pool named ContosoStaticIPAddressPool02 by using the **Get-WAPackStaticIPAddressPool** cmdlet, and then stores that object in the $ StaticIPAddressPool variable.</span></span>

<span data-ttu-id="0dd1a-117">Drugie polecenie usuwa statyczną pulę adresów IP przechowywaną w $StaticIPAddressPool.</span><span class="sxs-lookup"><span data-stu-id="0dd1a-117">The second command removes the static IP address pool stored in $StaticIPAddressPool.</span></span>
<span data-ttu-id="0dd1a-118">To polecenie zawiera parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="0dd1a-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="0dd1a-119">Polecenie nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0dd1a-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="0dd1a-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0dd1a-120">PARAMETERS</span></span>

### <span data-ttu-id="0dd1a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="0dd1a-121">-Force</span></span>
<span data-ttu-id="0dd1a-122">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0dd1a-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dd1a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0dd1a-123">-PassThru</span></span>
<span data-ttu-id="0dd1a-124">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="0dd1a-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0dd1a-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="0dd1a-125">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dd1a-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="0dd1a-126">-Profile</span></span>
<span data-ttu-id="0dd1a-127">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0dd1a-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0dd1a-128">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="0dd1a-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0dd1a-129">-StaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="0dd1a-129">-StaticIPAddressPool</span></span>
<span data-ttu-id="0dd1a-130">Określa StaticIPAddressPool.</span><span class="sxs-lookup"><span data-stu-id="0dd1a-130">Specifies a StaticIPAddressPool.</span></span>
<span data-ttu-id="0dd1a-131">Aby uzyskać statyczną pulę adresów IP, użyj polecenia cmdlet **Get-WAPackStaticIPAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="0dd1a-131">To obtain a static IP address pool, use the **Get-WAPackStaticIPAddressPool** cmdlet.</span></span>

```yaml
Type: StaticIPAddressPool
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0dd1a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dd1a-132">CommonParameters</span></span>
<span data-ttu-id="0dd1a-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dd1a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dd1a-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dd1a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dd1a-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0dd1a-135">INPUTS</span></span>

## <span data-ttu-id="0dd1a-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0dd1a-136">OUTPUTS</span></span>

## <span data-ttu-id="0dd1a-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0dd1a-137">NOTES</span></span>

## <span data-ttu-id="0dd1a-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0dd1a-138">RELATED LINKS</span></span>

[<span data-ttu-id="0dd1a-139">Get-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="0dd1a-139">Get-WAPackStaticIPAddressPool</span></span>](./Get-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="0dd1a-140">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="0dd1a-140">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


