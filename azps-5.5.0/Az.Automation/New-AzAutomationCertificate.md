---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
ms.openlocfilehash: c80eb16f840fb6d590c139a6ec4b30d73584b741
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201082"
---
# <span data-ttu-id="d6ccc-101">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="d6ccc-101">New-AzAutomationCertificate</span></span>

## <span data-ttu-id="d6ccc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6ccc-102">SYNOPSIS</span></span>
<span data-ttu-id="d6ccc-103">Tworzy certyfikat automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="d6ccc-103">Creates an Automation certificate.</span></span>

## <span data-ttu-id="d6ccc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d6ccc-104">SYNTAX</span></span>

```
New-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6ccc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d6ccc-105">DESCRIPTION</span></span>
<span data-ttu-id="d6ccc-106">Polecenie **cmdlet New-AzAutomationCertificate** tworzy certyfikat w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d6ccc-106">The **New-AzAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="d6ccc-107">Podaj ścieżkę do pliku certyfikatu, który chcesz przekazać.</span><span class="sxs-lookup"><span data-stu-id="d6ccc-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="d6ccc-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d6ccc-108">EXAMPLES</span></span>

### <span data-ttu-id="d6ccc-109">Przykład 1. Tworzenie nowego certyfikatu</span><span class="sxs-lookup"><span data-stu-id="d6ccc-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d6ccc-110">Pierwsze polecenie konwertuje hasło w formacie zwykłego tekstu na bezpieczny ciąg za pomocą ConvertTo-SecureString cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6ccc-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="d6ccc-111">Polecenie przechowuje ten obiekt w $Password zmienną.</span><span class="sxs-lookup"><span data-stu-id="d6ccc-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="d6ccc-112">Drugie polecenie tworzy certyfikat o nazwie ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="d6ccc-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="d6ccc-113">To polecenie używa hasła przechowywanego w $Password.</span><span class="sxs-lookup"><span data-stu-id="d6ccc-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="d6ccc-114">To polecenie określa nazwę konta i ścieżkę do pliku, który jest przesyłany.</span><span class="sxs-lookup"><span data-stu-id="d6ccc-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="d6ccc-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6ccc-115">PARAMETERS</span></span>

### <span data-ttu-id="d6ccc-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d6ccc-116">-AutomationAccountName</span></span>
<span data-ttu-id="d6ccc-117">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet przechowuje certyfikat.</span><span class="sxs-lookup"><span data-stu-id="d6ccc-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ccc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6ccc-118">-DefaultProfile</span></span>
<span data-ttu-id="d6ccc-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d6ccc-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6ccc-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="d6ccc-120">-Description</span></span>
<span data-ttu-id="d6ccc-121">Określa opis certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="d6ccc-121">Specifies a description for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ccc-122">-Exportable</span><span class="sxs-lookup"><span data-stu-id="d6ccc-122">-Exportable</span></span>
<span data-ttu-id="d6ccc-123">Określa, czy certyfikat można wyeksportować.</span><span class="sxs-lookup"><span data-stu-id="d6ccc-123">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ccc-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d6ccc-124">-Name</span></span>
<span data-ttu-id="d6ccc-125">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="d6ccc-125">Specifies the name for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ccc-126">— Hasło</span><span class="sxs-lookup"><span data-stu-id="d6ccc-126">-Password</span></span>
<span data-ttu-id="d6ccc-127">Określa hasło pliku certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="d6ccc-127">Specifies the password for the certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ccc-128">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="d6ccc-128">-Path</span></span>
<span data-ttu-id="d6ccc-129">Określa ścieżkę do pliku skryptu, który jest przesyłany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6ccc-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="d6ccc-130">Plik może być plikiem cer lub pfx.</span><span class="sxs-lookup"><span data-stu-id="d6ccc-130">The file can be a .cer or a .pfx file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ccc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6ccc-131">-ResourceGroupName</span></span>
<span data-ttu-id="d6ccc-132">Określa nazwę grupy zasobów, dla której to polecenie cmdlet tworzy certyfikat.</span><span class="sxs-lookup"><span data-stu-id="d6ccc-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ccc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6ccc-133">CommonParameters</span></span>
<span data-ttu-id="d6ccc-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6ccc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6ccc-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6ccc-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6ccc-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6ccc-136">INPUTS</span></span>

### <span data-ttu-id="d6ccc-137">System.String</span><span class="sxs-lookup"><span data-stu-id="d6ccc-137">System.String</span></span>

### <span data-ttu-id="d6ccc-138">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="d6ccc-138">System.Security.SecureString</span></span>

### <span data-ttu-id="d6ccc-139">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="d6ccc-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d6ccc-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6ccc-140">OUTPUTS</span></span>

### <span data-ttu-id="d6ccc-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="d6ccc-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="d6ccc-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d6ccc-142">NOTES</span></span>

<span data-ttu-id="d6ccc-143">To polecenie powinno być uruchamiane na komputerze, na których jesteś administratorem, oraz w sesji programu PowerShell o podwyższonym poziomie uprawnień. zanim certyfikat zostanie przekazany, to polecenie cmdlet użyje lokalnego magazynu X.509 do pobrania kciuka i klucza, a jeśli to polecenie cmdlet zostanie uruchomione poza sesją programu PowerShell o podwyższonym poziomie uprawnień, zostanie wyświetlony błąd "Odmowa dostępu".</span><span class="sxs-lookup"><span data-stu-id="d6ccc-143">This command should be run on a machine that you are an administrator of, as well as in an elevated PowerShell session; before the certificate is uploaded, this cmdlet uses the local X.509 store to retrieve the thumbprint and key, and if this cmdlet is run outside of an elevated PowerShell session, you will receive an "Access denied" error.</span></span>

## <span data-ttu-id="d6ccc-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6ccc-144">RELATED LINKS</span></span>

[<span data-ttu-id="d6ccc-145">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="d6ccc-145">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="d6ccc-146">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="d6ccc-146">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="d6ccc-147">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="d6ccc-147">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


