---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BFB57100-93F6-4FD2-8ECA-7F54BEB0D6B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7114f39ee2b105c80429151df8347b5c17dcfea0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055472"
---
# <span data-ttu-id="57377-101">Get-AzureWebsiteLog</span><span class="sxs-lookup"><span data-stu-id="57377-101">Get-AzureWebsiteLog</span></span>

## <span data-ttu-id="57377-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57377-102">SYNOPSIS</span></span>
<span data-ttu-id="57377-103">Pobiera dzienniki określonej witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="57377-103">Gets logs for the specified website.</span></span>

## <span data-ttu-id="57377-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57377-104">SYNTAX</span></span>

### <span data-ttu-id="57377-105">Ogonkiem</span><span class="sxs-lookup"><span data-stu-id="57377-105">Tail</span></span>
```
Get-AzureWebsiteLog [-Path <String>] [-Message <String>] [-Tail] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="57377-106">ListPath</span><span class="sxs-lookup"><span data-stu-id="57377-106">ListPath</span></span>
```
Get-AzureWebsiteLog [-ListPath] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="57377-107">Opis</span><span class="sxs-lookup"><span data-stu-id="57377-107">DESCRIPTION</span></span>
<span data-ttu-id="57377-108">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="57377-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="57377-109">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="57377-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="57377-110">Pobiera dziennik dla określonej witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="57377-110">Gets log for the specified website.</span></span>

## <span data-ttu-id="57377-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57377-111">EXAMPLES</span></span>

### <span data-ttu-id="57377-112">Przykład 1: Rozpoczynanie przesyłania strumieniowego dziennika</span><span class="sxs-lookup"><span data-stu-id="57377-112">Example 1: Start log streaming</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail
```

<span data-ttu-id="57377-113">W tym przykładzie rozpoczęto przesyłanie strumieniowe dziennika dla wszystkich dzienników aplikacji.</span><span class="sxs-lookup"><span data-stu-id="57377-113">This example starts log streaming for all application logs.</span></span>

### <span data-ttu-id="57377-114">Przykład 2: Rozpoczynanie przesyłania strumieniowego dziennika dla dzienników http</span><span class="sxs-lookup"><span data-stu-id="57377-114">Example 2: Start log streaming for http logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail -Path http
```

<span data-ttu-id="57377-115">W tym przykładzie Rozpoczynanie przesyłania strumieniowego dziennika dla dzienników http.</span><span class="sxs-lookup"><span data-stu-id="57377-115">This example starts log streaming for http logs.</span></span>

### <span data-ttu-id="57377-116">Przykład 3: Rozpoczynanie przesyłania strumieniowego dziennika dla dzienników błędów</span><span class="sxs-lookup"><span data-stu-id="57377-116">Example 3: Start log streaming for error logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail -Message Error
```

<span data-ttu-id="57377-117">W tym przykładzie Rozpoczynanie przesyłania strumieniowego dziennika i wyświetlanie tylko dzienników błędów.</span><span class="sxs-lookup"><span data-stu-id="57377-117">This example starts log streaming and show error logs only.</span></span>

### <span data-ttu-id="57377-118">Przykład 4: Wyświetlanie dzienników avaiable</span><span class="sxs-lookup"><span data-stu-id="57377-118">Example 4: Display avaiable logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Name MyWebsite -ListPath
```

<span data-ttu-id="57377-119">W tym przykładzie są wyświetlane wszystkie dostępne ścieżki dziennika w witrynie sieci Web.</span><span class="sxs-lookup"><span data-stu-id="57377-119">This example lists all available log paths in the website.</span></span>

## <span data-ttu-id="57377-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57377-120">PARAMETERS</span></span>

### <span data-ttu-id="57377-121">-ListPath</span><span class="sxs-lookup"><span data-stu-id="57377-121">-ListPath</span></span>
<span data-ttu-id="57377-122">Wskazuje, czy mają być wystawiane ścieżki dziennika.</span><span class="sxs-lookup"><span data-stu-id="57377-122">Indicates whether to list the log paths.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListPath
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57377-123">-Message</span><span class="sxs-lookup"><span data-stu-id="57377-123">-Message</span></span>
<span data-ttu-id="57377-124">Określa ciąg znaków, który zostanie zastosowany do filtrowania komunikatu dziennika.</span><span class="sxs-lookup"><span data-stu-id="57377-124">Specifies a string which will be used to filter the log message.</span></span>
<span data-ttu-id="57377-125">Zostaną pobrane tylko dzienniki zawierające ten ciąg.</span><span class="sxs-lookup"><span data-stu-id="57377-125">Only logs which contains this string will be retrieved.</span></span>

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57377-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="57377-126">-Name</span></span>
<span data-ttu-id="57377-127">Nazwa witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="57377-127">The name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57377-128">-Path</span><span class="sxs-lookup"><span data-stu-id="57377-128">-Path</span></span>
<span data-ttu-id="57377-129">Ścieżka, z której ma zostać pobrany dziennik.</span><span class="sxs-lookup"><span data-stu-id="57377-129">The path from which the log will be retrieved.</span></span>
<span data-ttu-id="57377-130">Domyślnie jest to element główny, co oznacza, że obejmuje wszystkie ścieżki.</span><span class="sxs-lookup"><span data-stu-id="57377-130">By default it is Root, which means include all the paths.</span></span>

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57377-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="57377-131">-Profile</span></span>
<span data-ttu-id="57377-132">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57377-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="57377-133">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="57377-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="57377-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="57377-134">-Slot</span></span>
<span data-ttu-id="57377-135">Określa nazwę gniazda.</span><span class="sxs-lookup"><span data-stu-id="57377-135">Specifies the slot name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57377-136">-Koniec</span><span class="sxs-lookup"><span data-stu-id="57377-136">-Tail</span></span>
<span data-ttu-id="57377-137">Określa, czy mają być przesyłane strumieniowo dzienniki.</span><span class="sxs-lookup"><span data-stu-id="57377-137">Specifies whether to stream the logs.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Tail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57377-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57377-138">CommonParameters</span></span>
<span data-ttu-id="57377-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57377-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57377-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57377-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57377-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57377-141">INPUTS</span></span>

## <span data-ttu-id="57377-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57377-142">OUTPUTS</span></span>

## <span data-ttu-id="57377-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57377-143">NOTES</span></span>

## <span data-ttu-id="57377-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57377-144">RELATED LINKS</span></span>

[<span data-ttu-id="57377-145">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="57377-145">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="57377-146">Nowe — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="57377-146">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="57377-147">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="57377-147">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="57377-148">Start — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="57377-148">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


