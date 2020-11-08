---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: FDA8BAAA-7C37-4BCB-9C02-EB6296C09C2B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 00904cc1b67c32bc3658c1c4f6e8b123a5601ff7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055188"
---
# <span data-ttu-id="2c438-101">New-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="2c438-101">New-AzureAutomationCertificate</span></span>

## <span data-ttu-id="2c438-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c438-102">SYNOPSIS</span></span>

<span data-ttu-id="2c438-103">Tworzy certyfikat usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="2c438-103">Creates an Azure Automation certificate.</span></span>

## <span data-ttu-id="2c438-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c438-104">SYNTAX</span></span>

```
New-AzureAutomationCertificate -Name <String> [-Description <String>] [-Password <SecureString>] -Path <String>
 [-Exportable] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2c438-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2c438-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="2c438-106">Polecenie cmdlet **New-AzureAutomationCertificate** tworzy certyfikat w usłudze Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="2c438-106">The **New-AzureAutomationCertificate** cmdlet creates a certificate in Microsoft Azure Automation.</span></span>
<span data-ttu-id="2c438-107">Podaj ścieżkę do pliku certyfikatu, który chcesz przekazać.</span><span class="sxs-lookup"><span data-stu-id="2c438-107">You provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="2c438-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c438-108">EXAMPLES</span></span>

### <span data-ttu-id="2c438-109">Przykład 1. Tworzenie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="2c438-109">Example 1: Create a certificate</span></span>
```
PS C:\> $password = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> New-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "MyCertificate" -Path "./cert.pfx" -Password $password
```

<span data-ttu-id="2c438-110">Te polecenia tworzą certyfikat w usłudze Azure Automation o nazwie webcertificate.</span><span class="sxs-lookup"><span data-stu-id="2c438-110">These commands create a certificate in Azure Automation named MyCertificate.</span></span>
<span data-ttu-id="2c438-111">Pierwsze polecenie tworzy hasło do pliku certyfikatu używanego w drugim poleceniu tworzącym certyfikat.</span><span class="sxs-lookup"><span data-stu-id="2c438-111">The first command creates the password for the certificate file that is used in the second command that creates the certificate.</span></span>

## <span data-ttu-id="2c438-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c438-112">PARAMETERS</span></span>

### <span data-ttu-id="2c438-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2c438-113">-AutomationAccountName</span></span>
<span data-ttu-id="2c438-114">Określa nazwę konta usługi Automation, w którym certyfikat będzie przechowywany.</span><span class="sxs-lookup"><span data-stu-id="2c438-114">Specifies the name of the Automation account the certificate will be stored in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c438-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="2c438-115">-Description</span></span>
<span data-ttu-id="2c438-116">Określa opis certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="2c438-116">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="2c438-117">— Możliwy do wyeksportowania</span><span class="sxs-lookup"><span data-stu-id="2c438-117">-Exportable</span></span>
<span data-ttu-id="2c438-118">Wskazuje, że certyfikat można wyeksportować.</span><span class="sxs-lookup"><span data-stu-id="2c438-118">Indicates the certificate can be exported.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c438-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2c438-119">-Name</span></span>
<span data-ttu-id="2c438-120">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="2c438-120">Specifies a name for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c438-121">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="2c438-121">-Password</span></span>
<span data-ttu-id="2c438-122">Określa hasło do pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="2c438-122">Specifies the password for the certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c438-123">-Path</span><span class="sxs-lookup"><span data-stu-id="2c438-123">-Path</span></span>
<span data-ttu-id="2c438-124">Określa ścieżkę do pliku skryptu, który ma zostać przekazany.</span><span class="sxs-lookup"><span data-stu-id="2c438-124">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="2c438-125">Plik może mieć nazwę cer lub PFX.</span><span class="sxs-lookup"><span data-stu-id="2c438-125">The file can be .cer or .pfx.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c438-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="2c438-126">-Profile</span></span>
<span data-ttu-id="2c438-127">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c438-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2c438-128">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="2c438-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2c438-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c438-129">CommonParameters</span></span>
<span data-ttu-id="2c438-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c438-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c438-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c438-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c438-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c438-132">INPUTS</span></span>

## <span data-ttu-id="2c438-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c438-133">OUTPUTS</span></span>

### <span data-ttu-id="2c438-134">Microsoft. Azure. Commands. Automation. model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="2c438-134">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="2c438-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c438-135">NOTES</span></span>

## <span data-ttu-id="2c438-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c438-136">RELATED LINKS</span></span>

[<span data-ttu-id="2c438-137">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="2c438-137">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="2c438-138">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="2c438-138">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)

[<span data-ttu-id="2c438-139">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="2c438-139">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


